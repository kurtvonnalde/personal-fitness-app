# 1 Create the Backend Solution and Projects

cd fitness-ai-app
mkdir -p apps/api/src
cd apps/api
dotnet new sln -n FitnessAI

## 1.1 Create the projects:

- cd src
- dotnet new webapi -n FitnessAI.Api
- dotnet new classlib -n FitnessAI.Application
- dotnet new classlib -n FitnessAI.Domain
- dotnet new classlib -n FitnessAI.Infrastructure

## 1.2 Go back to the solution folder and add them:

- cd ..
- dotnet sln add src/FitnessAI.Api/FitnessAI.Api.csproj
- dotnet sln add src/FitnessAI.Application/FitnessAI.Application.csproj
- dotnet sln add src/FitnessAI.Domain/FitnessAI.Domain.csproj
- dotnet sln add src/FitnessAI.Infrastructure/FitnessAI.Infrastructure.csproj

## 1.3 Add Project References

- dotnet add src/FitnessAI.Application/FitnessAI.Application.csproj reference src/FitnessAI.Domain/FitnessAI.Domain.csproj

- dotnet add src/FitnessAI.Infrastructure/FitnessAI.Infrastructure.csproj reference src/FitnessAI.Application/FitnessAI.Application.csproj
- dotnet add src/FitnessAI.Infrastructure/FitnessAI.Infrastructure.csproj reference src/FitnessAI.Domain/FitnessAI.Domain.csproj

- dotnet add src/FitnessAI.Api/FitnessAI.Api.csproj reference src/FitnessAI.Application/FitnessAI.Application.csproj
- dotnet add src/FitnessAI.Api/FitnessAI.Api.csproj reference src/FitnessAI.Infrastructure/FitnessAI.Infrastructure.csproj
 

# 2 Install NuGet Packages

## 2.1 Infrastructure packages

- dotnet add src/FitnessAI.Infrastructure/FitnessAI.Infrastructure.csproj package Microsoft.EntityFrameworkCore
- dotnet add src/FitnessAI.Infrastructure/FitnessAI.Infrastructure.csproj package Microsoft.EntityFrameworkCore.Design
- dotnet add src/FitnessAI.Infrastructure/FitnessAI.Infrastructure.csproj package Npgsql.EntityFrameworkCore.PostgreSQL
- dotnet add src/FitnessAI.Infrastructure/FitnessAI.Infrastructure.csproj package Microsoft.AspNetCore.Authentication.JwtBearer
- dotnet add src/FitnessAI.Infrastructure/FitnessAI.Infrastructure.csproj package Microsoft.Extensions.Identity.Core

## 2.2 API packages

- dotnet add src/FitnessAI.Api/FitnessAI.Api.csproj package Swashbuckle.AspNetCore