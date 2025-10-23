# ZENITH — PC Parts Store

This repo contains the backend skeleton for ZENITH — an e-commerce platform for gaming peripherals.

## Project
- Project name: **ZENITH**
- Goal: MVP to sell gaming mice, keyboards and accessories in India. Modular monolith (middleware <-> core) designed for future microservice extraction.

## Tech stack (planned)
- Java 17, Spring Boot (modular)
- PostgreSQL
- Docker + Docker Compose
- React (frontend)
- Razorpay (payments)
- S3-compatible storage for images
- GitHub Actions for CI

## Quick start (dev)

1. Copy `.env.example` to `.env` and update values (do NOT commit secrets).
2. Start Postgres and Adminer:
   ```bash
   docker-compose up -d postgres adminer
