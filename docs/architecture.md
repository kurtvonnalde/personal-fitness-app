# Architecture Overview

## Tech Stack

### Mobile
- React Native (Expo)
- Axios
- React Navigation

### Backend
- ASP.NET Core Web API
- Entity Framework Core
- JWT Authentication

### Database
- PostgreSQL (Azure)

### Cloud
- Azure App Service
- Azure PostgreSQL
- Azure OpenAI (later phase)

---

## System Architecture

Mobile App (Expo)
   |
   |--> ASP.NET Core API
           |
           |--> PostgreSQL
           |--> Azure OpenAI (AI insights)
           |--> Map Provider (Google Maps / Azure Maps)

---

## Key Modules

### Backend
- Auth Module
- Profile Module
- Activity Tracking Module
- Goal Module
- AI Insights Module

### Mobile
- Authentication Screens
- Activity Tracker Screen
- Map Screen
- Dashboard Screen
- AI Chat Screen