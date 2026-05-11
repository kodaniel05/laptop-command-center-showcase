# Engineering Decisions

## Local-First By Default

Laptop Command Center deals with highly sensitive personal storage metadata. The core architecture keeps scan data local and avoids making cloud upload a requirement.

## Metadata Over File Contents

The product is designed around file metadata, derived categories, and review state. This reduces privacy risk and keeps the workflow focused on storage decisions rather than content ingestion.

## Review Queues Instead Of Automatic Cleanup

The app surfaces candidates for review rather than presenting automation as certainty. This is especially important for old school files, repeated filenames, large documents, installers, and cache-like data where context matters.

## Guarded File Actions

File actions are routed through validation and confirmation flows. The app treats delete-like behavior conservatively and separates review status from destructive filesystem changes.

## Bounded Scans

Local filesystem scans can be expensive or hit protected folders. The private implementation accounts for scan modes, partial scan results, warnings, and bounded traversal to keep the app responsive.

## Dashboard-First Product Shape

The app is organized around the actions a user needs to take: review documents, inspect smart folders, search, understand storage, and review history. This keeps the UI practical and avoids burying the workflow inside a generic file explorer.

## Public Showcase Boundary

This repository is intentionally documentation-only. It communicates product judgment and engineering architecture without publishing reusable application code, internal schemas, local scan output, or proprietary logic.
