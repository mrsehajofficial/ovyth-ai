# ai

Talk to an OpenAI-compatible chat endpoint from Ovyth.

## Install

```bash
ovc pkg install ai
```

## Use

```ov
import "ai"
m = ai_conversation("be terse")
ai_ask(m, "what is ovyth?")
r = ai_request(url, key, model, m, 30.0)
if r["ok"] { print(r["text"]) } else { print("error: " + r["error"]) } 
```

## Conventions

Every public name is prefixed `ai_`: Ovyth flattens all top-level names
into one program, so the prefix *is* the namespace. Nothing here runs at
import time and the module holds no state between calls — the caller owns
the data and passes it in, which keeps it serializable and safe next to
other packages.

## License

MIT
