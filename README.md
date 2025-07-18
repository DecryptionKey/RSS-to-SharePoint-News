# 🛡️RSS to SharePoint News🛡️
<img width="1255" height="577" alt="image" src="https://github.com/user-attachments/assets/5931c41f-507e-4630-9f55-2d3b98c5d444" />

This project provides a Power Automate flow that automatically retrieves updates from RSS feeds and posts them as SharePoint News items. It enables seamless integration between external content sources and internal SharePoint communication systems.

## Overview

The flow triggers whenever an RSS feed is updated. It parses the incoming data (JSON or HTML) into plain text to ensure compatibility with SharePoint. The content is then posted as a news item using the SharePoint HTTP request connector and the SharePoint Repost API.

This solution is ideal for organizations that want to:
- Auto-publish content from trusted external sources
- Monitor industry updates or vulnerability advisories
- Keep internal teams informed without manual posting

## 🔧 Features

- Scheduled or event-based RSS polling
- Supports JSON and HTML-based RSS formats
- Plain text conversion for SharePoint compatibility
- Uses SharePoint HTTP request actions and Repost API
- Auto-creates SharePoint News items with title, summary, and link
- Lightweight and configurable

## 🔐Example Use Case

In a cybersecurity context, this flow can pull data from feeds like NVD (National Vulnerability Database) or CVE Details and post critical vulnerability disclosures to a SharePoint Security News hub.

## ✅Testing

The flow was tested in a development environment over multiple days. It successfully created SharePoint News posts for every new RSS item received, confirming stability and accuracy.

## 🚨 Requirements

- Microsoft Power Automate license
- SharePoint site with News Posts enabled
- RSS feed URL (e.g., blog, news, security advisory)
- Site and list permissions for SharePoint HTTP connector

## 📁 Setup Instructions

1. Import the `.zip` flow package into Power Automate.
2. Edit the flow to set your RSS feed URL.
3. Configure your SharePoint site URL and authentication.
4. Test the flow using a feed with frequent updates.
5. Enable the flow to run automatically on a schedule or trigger.

## 🔄 Customization

You can extend the flow to:
- Filter RSS items by keyword or category
- Tag news posts with metadata
- Send Teams notifications for high-priority items
- Format HTML content for rich SharePoint display

## ⚠️ Limitations

- Complex HTML formatting is stripped in plain text mode
- Rate-limited by RSS provider and SharePoint API quotas
- Requires proper SharePoint permissions for API use

## ⚖️ License

This project is open-source and provided under the MIT License.
