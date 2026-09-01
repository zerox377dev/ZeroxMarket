# ZeroxMarket

Private app distribution and auto-update marketplace for developer ecosystem.

## Purpose

Central hub for distributing apps, managing OTA updates, and hosting DNS allowlists for Firebase and other services used across all apps.

## How it works

Each app has its own directory with a `releases.json` manifest. Apps poll this manifest to check for updates and download new APKs.

## App Structure

```
/<app-name>/
  releases.json          Update manifest
  releases/              APK files for each version
```

## Updating a release

1. Place the new APK in `/<app-name>/releases/`
2. Update `releases.json` with the new version info and APK URL
3. Push to `main` — apps will detect the update on next launch

## AdGuard

DNS allowlists for Firebase and other services:

```
/adguard/firebase_allowlist.txt
```
