---
title: Custom GitHub Actions 101
author: Jan Macku
date: 2023-12-11
---

# Introduction

## What?

## But Why?

## How?

---

# What are GitHub Actions

> "GitHub Actions is a continuous integration and continuous delivery (CI/CD) platform that allows you to automate your build, test, and deployment pipeline. You can create workflows that build and test every pull request to your repository, or deploy merged pull requests to production." - [GitHub Docs](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions#overview)

- CI/CD platform integrated into GitHub
- Available for all public repositories for free
- [GitHub Marketplace](https://github.com/marketplace?category=&query=&type=actions&verification=) with more then 21k Actions

---

# Why write a custom GitHub Action

- To automate manual repetitive tasks and save time
- To improve the developer/user experience (real-time feedback)
- To integrate with internal/external services (Bugzilla, Jira)
- To speed up the development process (releases, deployments)
- To reduce the number of user errors (validation, SAST)

---

# How to create a custom GitHub Action

There are three types:

1. [Composite GitHub Action](https://docs.github.com/en/actions/creating-actions/about-custom-actions#composite-actions)
2. [Container based GitHub Action](https://docs.github.com/en/actions/creating-actions/about-custom-actions#docker-container-actions)
3. [JavaScript GitHub Action](https://docs.github.com/en/actions/creating-actions/about-custom-actions#javascript-actions)

The `action.{yml,yaml}` metadata file defines the structure of the Action.

> [!NOTE]
> Look at GitHub Marketplace before creating your custom Action. Someone may have already created something similar.

---

# Composite GitHub Action

## Pros

- Allows you to reuse existing GitHub Actions
- Easy and fast to create (no need to learn new language/tools)
- Allows you to apply the DRY principle

## Cons

- Harder to test
- Less suitable for complex actions

Example - [testing-farm-as-github-action](https://github.com/sclorg/testing-farm-as-github-action/blob/8df50f87e3c911bfa78f5ba98a65603908fdf77d/action.yml) by _sclorg_

---

# Container based GitHub Action

## Pros

- You are not limited to the GitHub Actions environment
- Allows you to use any language/tool you want
- Easier to test

## Cons

- More complex to setup and maintain

Example - [Differential ShellCheck](https://github.com/redhat-plumbers-in-action/differential-shellcheck) by _redhat-plumbers-in-action_

Templates - [Dockerfile](https://github.com/actions/container-action)

---

# JavaScript/TypeScript GitHub Action

## Pros

- Widely used by the community and by GitHub
- Large ecosystem of tools and libraries
- Easy to test
- Popular language

## Cons

- More complicated to setup
- JavaScript?

Example - [buildah-build](https://github.com/redhat-actions/buildah-build) by _redhat-actions_

Templates - [JavaScript](https://github.com/actions/javascript-action), [TypeScript](https://github.com/actions/typescript-action)

---

# Sources and further reading

- [GitHub Actions Security Best Practices](https://docs.github.com/en/actions/security-guides)

## Custom GitHub Actions

- [Custom GitHub Actions Documentation](https://docs.github.com/en/actions/creating-actions/about-custom-actions)
- [Composite GitHub Action](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action)
- [Container based GitHub Action](https://docs.github.com/en/actions/creating-actions/creating-a-docker-container-action)
- [JavaScript GitHub Action](https://docs.github.com/en/actions/creating-actions/creating-a-javascript-action)

## API

- [GitHub REST API](https://docs.github.com/en/rest)

---

# Thank you for your attention
