# QR Code Generator Service
A full-stack service that turns any URL into a PNG QR code, stores it on AWS S3, and returns a shareable link.
The project pairs a FastAPI backend with a React (Next.js) frontend, all containerised with Docker and delivered through a GitHub Actions CI/CD pipeline.

---

## Features
FastAPI endpoint accepts a URL, generates a QR image, and uploads it to S3

Next.js UI lets users enter a link and instantly preview / download the code

Environment-driven AWS credentials and region; public access handled by bucket policy

GitHub Actions workflow builds backend + frontend images and pushes to Docker Hub on every push to main

---

## Tech Stack
Frontend: React (Next.js), Axios, Tailwind CSS

Backend: Python 3.13, FastAPI, Uvicorn, qrcode, boto3

Cloud / Storage: AWS S3, IAM, public bucket policy

DevOps: Docker, Docker Hub, GitHub Actions CI/CD
