# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains the **OpenAPI 3.0.0 specification** for the Cloudglue API - a video analysis and processing platform by Aviary Inc. This is a specification-only repository; the single artifact is `spec/openapi.json`.

## Repository Structure

- `spec/openapi.json` - The complete OpenAPI specification (~11,000 lines, 47 endpoints, 108 schemas)
- No build system, package manager, or test suite - this is a declarative spec repository

## Common Tasks

**Editing the spec:** Directly modify `spec/openapi.json` to add/update endpoints, schemas, or documentation.

**Version bumps:** Update the `info.version` field in the spec when releasing changes.

## API Architecture

The Cloudglue API (base URL: `https://api.cloudglue.dev/v1`) organizes resources into these main categories:

- **Files** - Video file upload and management
- **Collections** - Grouping and organizing videos
- **Chat Completions** - AI-powered video Q&A
- **Transcriptions** - Audio-to-text jobs
- **Face Detection/Matching** - Facial recognition
- **Search** - Video content search
- **Segmentation** - Video segmentation and thumbnails
- **Extraction** - Structured data extraction from videos
- **Webhooks** - Event notifications

Authentication uses Bearer tokens.

## Git Workflow

- Main branch: `main`
- Use semantic commit messages (e.g., `docs: add new endpoint`, `fix: correct schema type`)
- PR-based workflow with PR numbers in commit messages

## External Resources

- API Documentation: https://docs.cloudglue.dev
- SDKs and Tools: https://github.com/aviaryhq
