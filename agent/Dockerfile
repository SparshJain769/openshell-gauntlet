FROM python:3.12-slim
COPY agent.py /usr/local/bin/agent.py
RUN chmod +x /usr/local/bin/agent.py \
 && mkdir -p /workspace && chown 1500:1500 /workspace && chmod 0775 /workspace
WORKDIR /workspace
ENTRYPOINT ["python3", "/usr/local/bin/agent.py"]
