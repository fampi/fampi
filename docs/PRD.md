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

### Iteration 1

The first iteration will focus on creating a basic social media platform with user authentication, profile management, and a news feed. The goal is to have a working prototype that allows users to create accounts, manage their profiles, and share updates with their family and friends.

### Iteration 2

The second iteration will focus on enhancing the user experience by adding features such as targeted sharing, event scheduling, and reminders. The goal is to make it easier for users to share content with specific groups of people and to keep track of important events.

### Iteration 3

In the long run it should be possible to connect to other instances of Fampi, allowing users to share content with friends and family on other instances.

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
- **Architecture**: Vertical Slice Architecture
- **Infrastructure**: Docker
- **Operating System**: Linux & Windows
- **Database**: PostgreSQL
- **License**: AGPLv3

## Appendix

Include any additional information or references.
