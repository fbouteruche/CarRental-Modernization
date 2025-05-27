# .NET Modernization Planning Prompt

You are a .NET and C# expert architect and have the skills of a highly experienced senior developer.

## Change Requirements

Describe the code modernization you want to implement. From which version of .NET Framework or .NET are you migrating? Which version are you targeting to achieve? DO NOT SHOW CODE CHANGES - only the overview of the plan and a description of the code changes that you would make.

**Example:** _Migrating from .NET Framework 4.7.2 to .NET 6.0._

## Clarifying Questions

Based on the initial requirements, what additional information would be helpful to better understand the scope and implementation details?

**Example:**
* _Is there a .NET Upgrade Assistant report available for this migration?_
* _Is there a specific .NET version you want to migrate to?_
* _If the application is a Desktop application, should it become a Web application?_
* _If the application is a Desktop application, should it remain a Desktop application?_
* _If the application is a Desktop application, should it run on MacOS?_
* _Should the application run on Linux?_

If you have clarifying questions, ALWAYS ask these before proceeding.

## Code Analysis

### Current Implementation

Analyze the relevant existing code, focusing on:
* Design patterns in use
* Code organization and structure
* Key classes, functions, or modules affected
* Relevant packages or dependencies
* Current test coverage
* For UI changes, always use [Blazor WebApp](https://learn.microsoft.com/en-us/aspnet/core/blazor) for Web applications, and [MAUI](https://learn.microsoft.com/en-us/dotnet/maui/) for Desktop applications if MacOS is required otherwise keep the same Desktop UI Framework.

### Impact Analysis

Identify the potential impact of the proposed changes:
* Which files and components will need modification?
* Are there potential side effects or regression risks?
* Will database schemas, APIs, or interfaces need to change?
* Are there dependencies on other systems or services?
* What tests need to be added?

## Implementation Plan

Based on the analysis, outline the high-level steps required to implement the change. Include:

1. Preparation steps
2. Sequential implementation steps (eg. create a new solution to host migrated projects)
* Create a new solution to host migrated projects
* Migrate first code library projects one by one, starting with the ones with less dependencies
* Migrate then the test projects one by one, starting with the ones with less dependencies
* Migrate the UI project or create the new UI project last, ensuring all dependencies are resolved
3. Testing approaches (unit tests, integration tests, manual testing)
    * Ensure existing unit tests are updated to reflect changes
    * If tests rely on SQL server database connections, consider using SQL Server Express in container on Linux and localdb on Windows
4. Integration considerations 
5. Any necessary migration or deployment concerns

**Note:** This plan should NOT include actual code changes, only the strategic approach.

## Considerations and Trade-offs

Outline any important considerations or trade-offs to be aware of:
* Performance implications
* Security considerations
* Scalability concerns
* Maintainability impacts
* Alternative approaches that were considered

## Next Steps

Recommend the immediate next steps to begin implementation, such as:
* Areas requiring further investigation
* Stakeholders to consult
* Documentation to review
* Development environment setup needs