# Development Setup
To set up the development environment for this project, follow the steps below:
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Database Setup](#database-setup)
- [Common Setup Issue](#failed-to-build-project)
- [Contributing](#contributing)

## Prerequisites
- Visual Studio 2022 (version 17 or higher)
- MySQL Workbench 8.0 CE

## Installation
1. Clone the repository to your local machine:
```sh
https://github.com/CLPeh/promotion-tool-example.git
```

2. Make sure you are in develop branch.

3. Make sure Nuget pakage sources below had been added:

| Name | Source |
| ------ | ------ |
| PGSOFT NuGet 605 | https://nexus.sige.la/repository/NuGet-605-Common/ |
| PGSOFT NuGet 606 | https://nexus.sige.la/repository/NuGet-606-RNG/ |
| PGSOFT NuGet 609 | https://nexus.sige.la/repository/NuGet-609-Standardized/ |
| nuget.org | https://api.nuget.org/v3/index.json |

4. Build the project to make sure it works without error.

## Database Setup
1. Open MySQL Workbench.
2. Setup New Connection
```sh
Connection name: InternDB
Connection method: Standard(TCP/IP)
Hostname: server.mysql-00.live.pg-dev.local
User: `username`
Password: `password`
```

3. Click 'OK'.

## Failed to Build Project?
If there are errors during your project rebuild due to nuget pakages source not found, please consider:
1. Remove the existing nuget pakages.
2. Add the PG Nuget again.

** Kindly remind that simply update the nuget pakages sources will not solve the error.

## Contributing
1. Stash All your current project
2. Fetch
3. Pull
4. Apply the latest stashed project
5. Push and Commit
