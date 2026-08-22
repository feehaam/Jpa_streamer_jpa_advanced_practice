# JPA Streamer vs Traditional JPA — Query Optimization

A hands-on Spring Boot project that benchmarks **JPA Streamer** (stream-based JPA queries) against traditional Spring Data JPA repository methods, using a realistic product domain (products, variants, tags, photos).

## Overview

The same product-retrieval use cases are implemented twice — once with regular derived/JPQL queries (`ProductRepositoryTraditional`) and once with JPA Streamer's `Stream>JPAAttribute>`-style predicates (`ProductRepositoryJPAStreamer`) — so query readability, lazy handling, and performance can be compared side by side. A shared `ProductService` interface with two implementations keeps the comparison fair.

## Tech Stack
- Java, Spring Boot (Web, Data JPA)
- [JPA Streamer](https://speedment.org/jpa-streamer/)
- PostgreSQL (docker-compose), Gradle

## Getting Started
```bash
docker compose up -d     # start PostgreSQL
./gradlew bootRun        # start the application
```

## What It Covers
- Side-by-side traditional Spring Data JPA vs JPA Streamer repositories
- Stream-based filtering/predicates over JPA entities
- Shared service abstraction with two interchangeable implementations
- Product domain model: Product, Variant, Tag, Photo
- Dockerized PostgreSQL for local runs

<!-- sync-marker-1 -->
