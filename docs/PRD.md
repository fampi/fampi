# Product Requirements Document (PRD)

## Project Overview

- **Project Name**: Fampi Blazor
- **Date**: May 2, 2025
- **Author**: Niklas Lagergren
- **Version**: 1.0
- **Status**: Draft
- **Last Updated**: May 2, 2025

## Objective

A private social media platform for family and friends, designed to be self-hosted and user-friendly. The goal is to create a platform that allows users to share updates, photos, and events with their close circle without the privacy concerns associated with larger social media platforms.

### Iteration 0 - Proof of Concept

To get the Proof of Concept (PoC) up and running quickly while maintaining a good appearance,, the following strategies will be employed:

1. **Use a UI Component Library**: Leverage the [Radzen](https://blazor.radzen.com/) UI component library.

2. **Focus on Core Features**: Implement only the essential UI components required for the PoC, such as:

   - Authentication and user management forms.
   - A basic news feed layout.
   - Profile management pages.
   - A simple post creation form.

3. **Responsive Design**: Ensure the UI is responsive by using the grid system or layout components provided by the chosen library.

4. **Minimal Customization**: Stick to the default themes and styles provided by the library to save time. Customization can be done later if needed.

5. **Iterative Development**: Start with functional components and refine the UI based on feedback during the PoC phase.

### Iteration 1 - Fully working news feed

The first iteration will focus on creating a basic social media platform with user authentication, profile management, and a news feed. The goal is to have a working prototype that allows users to create accounts, manage their profiles, and share updates with their family and friends.

### Iteration 2 - Targeted sharing and event scheduling

The second iteration will focus on enhancing the user experience by adding features such as targeted sharing, event scheduling, and reminders. The goal is to make it easier for users to share content with specific groups of people and to keep track of important events.

### Iteration 3 - Cross-instance sharing

In the long run it should be possible to connect to other instances of Fampi, allowing users to share content with friends and family on other instances.

This could be done through a federation system, where users can connect their accounts across different instances and share content seamlessly. This would require a robust API and authentication system to ensure secure connections between instances.

Existing protocols like ActivityPub, the AT Protocol or OStatus could be explored for inspiration, but the implementation would need to be tailored to the specific needs of Fampi. The solution for Fampi should be simpler than these protocols, as there are no decentralized needs.

### Iteration 4 - Extensibility

Extensibility in the form of plugins or modules to allow for future growth and customization. This could include features like food recipes, movie and tv-series watched, books read, or integration with other services.

### Iteration 5 - Marketplace

A central hub for admins to discover and install plugins or modules. And for verified developers to publish their plugins or modules.

## Key Features

### Authentication and User Management

A secure authentication system that allows admins to create accounts, manage profiles, and control privacy settings.

#### User registration and login

1. Users can only join the platform through an invitation link.
2. Admins can create user accounts and send invitations.
3. Users can log in using their email and password.
4. Password recovery options are available.
5. Two-factor authentication (2FA) is optional for added security.
6. User roles (admin, user) can be assigned to control access to features.
7. Admins can manage user accounts, including activation, deactivation, and deletion.

#### User groups

A user must belong to a user group. The default groups that are created are "Family", "Extended Family", and "Family Friends". The groups can be connected to another user group. The default groups are connected so that "Family" is the parent group of "Extended Family", which in turn is the parent group of "Family Friends". This means that if a user is part of "Family", they are also part of "Extended Family" and "Family Friends".

1. Admins can create, edit, and delete user groups.
2. Admins can assign and remove users to/from groups.
3. Admins can connect groups to each other, creating a hierarchy of groups.

#### Personal posts

In addition to the user groups, users can also create personal posts that are not shared with any user group. These posts are only visible to the user who created them. This serves as a personal diary or journal, allowing users to keep track of their thoughts and experiences without sharing them with others.

The personal posts needs to be encrypted and stored in a secure way, so that only the user who created them can access them. This can be done using client-side encryption, where the encryption key is stored in the user's browser and not on the server.

To be able to create personal posts the user must generate a key pair. The public key is stored on the server and the private key is stored in the user's browser. The private key is used to encrypt the personal posts before they are sent to the server. The server only stores the encrypted posts and does not have access to the private key.

If the user loses their private key, they will not be able to access their personal posts. Therefore, it is important to provide a way for the user to back up their private key. This can be done by allowing the user to download the private key as a file or by providing a way to export the key to a password manager.

Additionally, users should be informed about the importance of keeping their private key secure and the potential risks of losing it.

### Profile management

Users can update their profiles, including changing passwords , date of birth, and profile pictures.

### News feed

A central hub for users to see updates from their friends and family. The feed will display posts, photos, and events in a chronological order.

### Create and manage posts

Users can create, edit, and delete posts. Posts can include text, photos, and links. Users can also comment on and like posts.

### Targeted sharing

Users can choose what user group(s) that can see their posts, allowing for targeted sharing with predefined user groups setup by the admin. The selection should visually indicate the parent group(s) of the selected group.

#### Event scheduling and reminders

TBD.

## Target Audience

The target audience to begin with is a tech-savvy family member who is interested in self-hosting a social media platform for their family and friends. The platform should be easy to set up and use, even for those who may not be familiar with self-hosting.

The second target audience is the family and friends of the tech-savvy family member. They should be able to use the platform without needing to understand the technical details of self-hosting.

## Technical Requirements

- **Framework**: .NET Core 9 Blazor
- **Mode**: Blazor Interactive Server
- **Language**: C#
- **Bootstrap**: Use .NET Aspire to bootstrap the application.
- **Architecture**: Vertical Slice Architecture
- **Infrastructure**: Docker
- **Operating System**: Linux & Windows
- **Database**: PostgreSQL
- **License**: AGPLv3
- **Design**: Responsive design for mobile and desktop
- **Accessibility**: Compliance with WCAG 2.1 standards
- **Security**: Secure authentication, data encryption, and regular security audits
- **Performance**: Fast loading times and efficient database queries
- **UI Library\***: Radzen Blazor Components
- **Dev Commands**: Use .csproj file to create custom dev commands using the DotNetCliToolReference.

## Appendix

Include any additional information or references.
