---
title: Azure DevOps and TFS Package Management
description: Configuring GitHub repositories as Octopus Feeds
position: 60
---

With Azure DevOps and TFS package management, Octopus can consume either v2 or v3 NuGet feeds.

Learn more about [Azure DevOps or TFS Package Management](https://www.visualstudio.com/en-us/docs/package/overview).

## Connect Octopus to an Azure DevOps Package Feed

If you are using Azure DevOps Package Management, Octopus can consume either the v2 or v3 NuGet feeds.

- To connect to the v3 URL, you must use [a Personal Access Token](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) in the password field. The username field is not checked, so you can put anything in here as long as it is not blank. Ensure that the personal access token has (at least) the *Packaging (read)* scope.
- To connect to the v2 URL, you can use either [alternate credentials or a Personal Access Token](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) in the password field.

## Connect Octopus to a TFS Package Feed

If you are using TFS Package Management, Octopus can consume either the v2 or v3 NuGet feeds. Use a user account's username and password to authenticate.

Although the TFS documentation states that a Personal Access Token can be used, we have not had success authenticating using one with `NuGet.exe`.
