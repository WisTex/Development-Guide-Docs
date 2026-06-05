---

title: "Hubzilla Common Navigation Links Reference"
slug: "hubzilla-common-navigation-links"
version: "1.0"
status: "unpublished"
category: "Hubzilla"
author: "Scott M. Stolz"
license: "MIT"
copyright: "WisTex TechSero Ltd. Co."
tags: ["Hubzilla", "Navigation", "Themes", "URLs"]

---

# Hubzilla Common Navigation Links Reference

Version: 1.0

<hr>

## Purpose

This document provides a reference for commonly used Hubzilla pages and URLs.

It is intended for:

* Theme developers
* Template designers
* Developers
* Site administrators

Hubzilla themes can completely replace the default navigation. This reference helps identify common destinations that may be included in custom navigation menus, dashboards, landing pages, and application interfaces.

Some features may need to be enabled before the associated URLs become available. Availability may depend on site configuration, installed applications, channel permissions, or enabled features.

<hr>

## Communications

| Feature           | URL Pattern           | Description                                       |
| ----------------- | --------------------- | ------------------------------------------------- |
| Headquarters (HQ) | `/hq`                 | View notifications and incoming posts.            |
| Create a New Post | `/rpost`              | Create a new post, direct message, or forum post. |
| Channel           | `/channel/[nickname]` | View your channel and published content.          |
| Stream / Inbox    | `/network`            | View posts from people you follow.                |
| Starred Posts     | `/network/?f=&star=1` | View posts you have saved for future reference.   |
| Comment History   | `/network/?f=&conv=1` | View posts and comments you have participated in. |
| Direct Messages   | `/network/?f=&dm=1`   | View private conversations.                       |

## Contacts

| Feature             | URL Pattern            | Description                                       |
| ------------------- | ---------------------- | ------------------------------------------------- |
| Connections         | `/connections`         | Manage people and channels you follow.            |
| Connection Requests | `/connections/pending` | Review pending connection requests.               |
| Contact Roles       | `/permcats`            | Create groups of contacts and assign permissions. |

## Channel Features

| Feature       | URL Pattern           | Description                                 |
| ------------- | --------------------- | ------------------------------------------- |
| Channel       | `/channel/[nickname]` | View your channel.                          |
| Profile       | `/profile/[nickname]` | View your profile.                          |
| Photos        | `/photos/[nickname]`  | View photo albums and images.               |
| Calendar      | `/cdav/calendar`      | View events and appointments.               |
| Cloud Storage | `/cloud/[nickname]`   | View files, documents, and uploads.         |
| Apps          | `/apps`               | Manage available applications and features. |

## Configuration

| Feature         | URL Pattern                       | Description                                              |
| --------------- | --------------------------------- | -------------------------------------------------------- |
| Edit Profile    | `/profiles`                       | Manage profiles and avatars.                             |
| Settings        | `/settings`                       | Change channel settings.                                 |
| Features        | `/settings/features`              | Enable and disable available features.                   |
| Federation      | `/apps/available/?cat=Federation` | Manage federation-related applications and protocols.    |
| Theme           | `/settings/display`               | Change appearance and theme settings.                    |
| Manage Channels | `/manage`                         | Manage multiple channels (identities) under one account. |

## Networks

Hubzilla supports multiple communication protocols and networks.

| Feature     | URL Pattern | Description                                                                                 |
| ----------- | ----------- | ------------------------------------------------------------------------------------------- |
| ActivityPub | `/pubcrawl` | Connect with Mastodon, Pixelfed, PeerTube, Lemmy, Misskey, and other ActivityPub platforms. |
| Diaspora    | `/diaspora` | Connect with the Diaspora network.                                                          |
| Zot Network | Built In    | Connect with Hubzilla and Streams users through Hubzilla's native federation network.       |

<hr>

## Scope

This document focuses on commonly used navigation links and URLs.

It is not intended to document:

* Hubzilla architecture
* Permissions
* Core versus addon implementation details
* Theme development techniques
* Internal routing behavior

Those topics may be covered in separate documents.

<hr>

## Version History

| Version | Date       | Notes            |
| ------- | ---------- | ---------------- |
| 1.0     | 2026-06-05 | Initial release. |
