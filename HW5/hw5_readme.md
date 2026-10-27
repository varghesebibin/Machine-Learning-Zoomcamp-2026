# Homework 5 - Deployment

## Answers

- **Q1:** uv 0.13.5
- **Q2:** 1.7.2 (scikit-learn version)
- **Q3:** 0.533 (conversion probability for Q3 lead)
- **Q4:** 0.770 (conversion probability via FastAPI server)
- **Q5:** python:3.11.15-slim-bookworm (base image in Dockerfile)
- **Q6:** 0.770 (conversion probability via Docker container)

## What I did

1. Installed uv and set up the project environment using `uv sync --locked`
2. Verified the pickle model file via SHA256 checksum
3. Wrote `q3_solution.py` to load the model and predict for a single lead (Q3)
4. Started the FastAPI server with uvicorn and sent a prediction request via curl (Q4)
5. Inspected the Dockerfile to identify the base image (Q5)
6. Built the Docker image with `docker build -t zoomcamp-model:2026-hw5 .`
7. Ran the container with `docker run --rm -p 9696:9696 zoomcamp-model:2026-hw5`
8. Confirmed the containerized server returned the same prediction as the local server (Q6)

## Files

- `q3_solution.py` - script for Q3
- `hw5_readme.md` - this file
