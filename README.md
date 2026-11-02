# loop-a-local-llm
Building Loop, a local conversational LLM with a distinct personality, persistent memory, and an evolving architecture. An experiment in conversational identity, continuity, and human-AI interaction.

## Run Loop with Ollama

From this repository, with Ollama installed and running:

```sh
ollama pull gemma3:4b
ollama create loop -f Modelfile
ollama run loop
```

`Modelfile` uses Gemma 3 4B, sets temperature to `0.9`, and includes the
full personality from `loop.yaml` as structured system instructions. It uses
the base model's chat template and other default parameters.

If you edit the personality in `loop.yaml`, update the `SYSTEM` block in
`Modelfile` too, then rerun `ollama create loop -f Modelfile`. Ollama does
not read `loop.yaml` automatically.

This configures behavior; it does not train the model, add persistent memory,
or connect research tools. Those features require application support.

Modelfile syntax: [Ollama documentation](https://docs.ollama.com/modelfile).
