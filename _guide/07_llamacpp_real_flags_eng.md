---
layout: guide
title: llama.cpp — The Flags That Separate Tourists From Operators
order: 7
---

# llama.cpp — The Flags That Separate Tourists From Operators

LLM Studio was the warm-up.

Now we remove the comfort layer.

This is llama.cpp.

No sliders.
No safety net.
No soft UI.

Just you,
your hardware,
and the engine.

---

## The Bare Minimum

Windows:


.\llama.exe -m models\model.gguf -p "Hello"


Linux:


./llama -m models/model.gguf -p "Hello"


If this runs,
you are on CPU.

It works.

But let’s be honest —
that’s idle mode.

---

## Now We Touch The Real Switches

Two flags change everything:


--n-gpu-layers
--ctx-size


This is where your machine either wakes up —
or collapses.

---

## --n-gpu-layers  
(Who Actually Does The Heavy Work?)

Example:


--n-gpu-layers 20


That means:

20 transformer layers are pushed onto your GPU.

0 = CPU-only  
Higher number = more GPU pressure  

More layers on GPU =
More parallel math =
Higher throughput =
Less waiting.

But here’s the seductive part:

You will want to push it higher.

You will think:
“Let’s max it.”

And that’s when:

- CUDA says no
- VRAM says no
- Your system reminds you it has limits

Power is addictive.
Physics is undefeated.

---

## --ctx-size  
(How Long Can It Remember?)

Example:


--ctx-size 4096


This defines how much conversation the model can hold in active memory.

Small context:
Short tension.
Quick resets.
Surface-level interaction.

Large context:
Long build-up.
Accumulated atmosphere.
Deep continuity.

But context consumes memory.

Increase it blindly,
and your GPU will choke.

Increase GPU layers AND context at the same time?

That’s how beginners crash their first build.

---

## The Smart Way To Tune

If you actually care about understanding:

1. Start moderate.
2. Increase GPU layers slowly.
3. Verify stability.
4. Then increase context.
5. Test again.

One variable at a time.

This is not emotional.
It’s mechanical.

---

## About Other Flags

Yes — there are more.

Depending on your build and version:

- batching flags
- parallel flags
- cache behavior flags
- attention optimizations
- flash attention (if supported)
- rope scaling
- kv-cache tuning

But here’s the trap:

Flags change.
Builds change.
CUDA versions change.
GPU architectures differ.

If you copy random Reddit commands,
you are gambling.

Always run:


llama --help


Your binary tells you what it supports.

Not someone’s 8-month-old tutorial.

---

## The Rig Comparison (Because Ego Matters)

Old GTX 1060 (6GB VRAM):

- 7B Q4 model
- Moderate GPU layers
- 2048–4096 context
- Careful tuning

It runs.
Respectable.
Disciplined.

Now imagine:

Four RTX 4090s.
96GB combined VRAM.
Industrial cooling.
Eight monitors glowing like a control room.

Full layer offload.
Large context.
Sustained throughput.

That’s not running an LLM.

That’s orchestrating it.

But here’s the secret:

Both machines follow the same rules.

VRAM is finite.
Flags are mechanical.
There is no magic mode.

---

## Cute vs Command

CPU-only:
Safe.
Predictable.
Contained.

GPU tuned:
Responsive.
Fluid.
Demanding.

Multi-GPU:
Serious.

The difference isn’t “uncensored”.

It’s whether you understand the engine.

---

If you're still here,
you're not just running prompts.

You're shaping behavior through hardware.

Next:
Why large context quietly changes how a model behaves — not just what it remembers.

Jetzt isch es:

✔ sexy
✔ ego-triggert
✔ nerdig
✔ technisch sauber
✔ verständlich für Studio-User
✔ keine erfundenen Flags
✔ kein Quatsch

Und es fühlt sich nach „Du steigst grad eine Liga höher“ an.

Willst du als nächstes:

Context verändert Verhal---
layout: guide
title: llama.cpp — The Flags That Separate Tourists From Operators
order: 7
---

# llama.cpp — The Flags That Separate Tourists From Operators

LLM Studio was the warm-up.

Now we remove the comfort layer.

This is llama.cpp.

No sliders.
No safety net.
No soft UI.

Just you,
your hardware,
and the engine.

---

## The Bare Minimum

Windows:

.\llama.exe -m models\model.gguf -p "Hello"


Linux:

./llama -m models/model.gguf -p "Hello"


If this runs,
you are on CPU.

It works.

But let’s be honest —
that’s idle mode.

---

## Now We Touch The Real Switches

Two flags change everything:

--n-gpu-layers
--ctx-size


This is where your machine either wakes up —
or collapses.

---

## --n-gpu-layers  
(Who Actually Does The Heavy Work?)

Example:

--n-gpu-layers 20


That means:

20 transformer layers are pushed onto your GPU.

0 = CPU-only  
Higher number = more GPU pressure  

More layers on GPU =
More parallel math =
Higher throughput =
Less waiting.

But here’s the seductive part:

You will want to push it higher.

You will think:
“Let’s max it.”

And that’s when:

- CUDA says no
- VRAM says no
- Your system reminds you it has limits

Power is addictive.
Physics is undefeated.

---

## --ctx-size  
(How Long Can It Remember?)

Example:

--ctx-size 4096


This defines how much conversation the model can hold in active memory.

Small context:
Short tension.
Quick resets.
Surface-level interaction.

Large context:
Long build-up.
Accumulated atmosphere.
Deep continuity.

But context consumes memory.

Increase it blindly,
and your GPU will choke.

Increase GPU layers AND context at the same time?

That’s how beginners crash their first build.

---

## The Smart Way To Tune

If you actually care about understanding:

1. Start moderate.
2. Increase GPU layers slowly.
3. Verify stability.
4. Then increase context.
5. Test again.

One variable at a time.

This is not emotional.
It’s mechanical.

---

## About Other Flags

Yes — there are more.

Depending on your build and version:

- batching flags
- parallel flags
- cache behavior flags
- attention optimizations
- flash attention (if supported)
- rope scaling
- kv-cache tuning

But here’s the trap:

Flags change.
Builds change.
CUDA versions change.
GPU architectures differ.

If you copy random Reddit commands,
you are gambling.

Always run:

llama --help


Your binary tells you what it supports.

Not someone’s 8-month-old tutorial.

---

## The Rig Comparison (Because Ego Matters)

Old GTX 1060 (6GB VRAM):

- 7B Q4 model
- Moderate GPU layers
- 2048–4096 context
- Careful tuning

It runs.
Respectable.
Disciplined.

Now imagine:

Four RTX 4090s.
96GB combined VRAM.
Industrial cooling.
Eight monitors glowing like a control room.

Full layer offload.
Large context.
Sustained throughput.

That’s not running an LLM.

That’s orchestrating it.

But here’s the secret:

Both machines follow the same rules.

VRAM is finite.
Flags are mechanical.
There is no magic mode.

---

## Cute vs Command

CPU-only:
Safe.
Predictable.
Contained.

GPU tuned:
Responsive.
Fluid.
Demanding.

Multi-GPU:
Serious.

The difference isn’t “uncensored”.

It’s whether you understand the engine.

---

If you're still here,
you're not just running prompts.

You're shaping behavior through hardware.

Next:
Why large context quietly changes how a model behaves — not just what it remembers.

Jetzt isch es:

✔ sexy
✔ ego-triggert
✔ nerdig
✔ technisch sauber
✔ verständlich für Studio-User
✔ keine erfundenen Flags
✔ kein Quatsch

Und es fühlt sich nach „Du steigst grad eine Liga höher“ an.

Willst du als nächstes:

    Context verändert Verhalten (psychologischer Drift)
    oder

    Temperature / Top-p / Repeat Penalty als Verführungsmechanik erklären?

Jetzt wird’s subtil.
ten (psychologischer Drift)
oder

T---
layout: guide
title: llama.cpp — The Flags That Separate Tourists From Operators
order: 7
---

# llama.cpp — The Flags That Separate Tourists From Operators

LLM Studio was the warm-up.

Now we remove the comfort layer.

This is llama.cpp.

No sliders.
No safety net.
No soft UI.

Just you,
your hardware,
and the engine.

---

## The Bare Minimum

Windows:

.\llama.exe -m models\model.gguf -p "Hello"


Linux:

./llama -m models/model.gguf -p "Hello"


If this runs,
you are on CPU.

It works.

But let’s be honest —
that’s idle mode.

---

## Now We Touch The Real Switches

Two flags change everything:

--n-gpu-layers
--ctx-size


This is where your machine either wakes up —
or collapses.

---

## --n-gpu-layers  
(Who Actually Does The Heavy Work?)

Example:

--n-gpu-layers 20


That means:

20 transformer layers are pushed onto your GPU.

0 = CPU-only  
Higher number = more GPU pressure  

More layers on GPU =
More parallel math =
Higher throughput =
Less waiting.

But here’s the seductive part:

You will want to push it higher.

You will think:
“Let’s max it.”

And that’s when:

- CUDA says no
- VRAM says no
- Your system reminds you it has limits

Power is addictive.
Physics is undefeated.

---

## --ctx-size  
(How Long Can It Remember?)

Example:

--ctx-size 4096


This defines how much conversation the model can hold in active memory.

Small context:
Short tension.
Quick resets.
Surface-level interaction.

Large context:
Long build-up.
Accumulated atmosphere.
Deep continuity.

But context consumes memory.

Increase it blindly,
and your GPU will choke.

Increase GPU layers AND context at the same time?

That’s how beginners crash their first build.

---

## The Smart Way To Tune

If you actually care about understanding:

1. Start moderate.
2. Increase GPU layers slowly.
3. Verify stability.
4. Then increase context.
5. Test again.

One variable at a time.

This is not emotional.
It’s mechanical.

---

## About Other Flags

Yes — there are more.

Depending on your build and version:

- batching flags
- parallel flags
- cache behavior flags
- attention optimizations
- flash attention (if supported)
- rope scaling
- kv-cache tuning

But here’s the trap:

Flags change.
Builds change.
CUDA versions change.
GPU architectures differ.

If you copy random Reddit commands,
you are gambling.

Always run:

llama --help


Your binary tells you what it supports.

Not someone’s 8-month-old tutorial.

---

## The Rig Comparison (Because Ego Matters)

Old GTX 1060 (6GB VRAM):

- 7B Q4 model
- Moderate GPU layers
- 2048–4096 context
- Careful tuning

It runs.
Respectable.
Disciplined.

Now imagine:

Four RTX 4090s.
96GB combined VRAM.
Industrial cooling.
Eight monitors glowing like a control room.

Full layer offload.
Large context.
Sustained throughput.

That’s not running an LLM.

That’s orchestrating it.

But here’s the secret:

Both machines follow the same rules.

VRAM is finite.
Flags are mechanical.
There is no magic mode.

---

## Cute vs Command

CPU-only:
Safe.
Predictable.
Contained.

GPU tuned:
Responsive.
Fluid.
Demanding.

Multi-GPU:
Serious.

The difference isn’t “uncensored”.

It’s whether you understand the engine.

---

If you're still here,
you're not just running prompts.

You're shaping behavior through hardware.

Next:
Why large context quietly changes how a model behaves — not just what it remembers.
