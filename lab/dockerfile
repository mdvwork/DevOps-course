FROM python:3.11-slim
LABEL course.student="devops-student"
WORKDIR /lab

RUN mkdir -p /data && \
    useradd -u 1000 appuser && \
    chown -R appuser:appuser /lab /data

COPY --chown=appuser:appuser . /lab
USER appuser
EXPOSE 8000

CMD ["python", "app.py"]