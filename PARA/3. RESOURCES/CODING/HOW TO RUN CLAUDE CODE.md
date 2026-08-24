
Tags: [[Artificial Intelligence (AI)]] [[CODING]] 

---
### STEP 1

cd ~/free-claude-code

```BASH
uv run uvicorn server:app --host 0.0.0.0 --port 8082
```

### STEP 2

cd ~/your/desired/directory/to/run/claude-code/

```BASH
ANTHROPIC_AUTH_TOKEN="freecc" ANTHROPIC_BASE_URL="http://localhost:8082" claude
```


# RESOURCE

---

memory-management , knowledge-synthesis, search, search-strategy, writing-spec, content-creation, 