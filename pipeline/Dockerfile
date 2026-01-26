FROM python:3.13.11-slim

RUN pip install pandas pyarrow

# Copy uv binary from official uv image (multi-stage build pattern)
COPY --from=ghcr.io/astral-sh/uv:latest /uv /bin/

WORKDIR /code

COPY pipeline.py .

ENTRYPOINT ["python", "pipeline.py"]