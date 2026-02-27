---
layout: guide
title: Sampling, Context and Hardware — The Behavioral Control Layer
order: 10
---

# Sampling, Context and Hardware — The Behavioral Control Layer

You tuned GPU layers.

You increased context.

You changed temperature.

And suddenly the model feels different.

Not smarter.

Not bigger.

Different.

This is where most users lose control.

Because they don’t realize they’re no longer “running a model”.

They are shaping probability under pressure.

---

## The Control Stack (Read This Slowly)

There are four forces shaping output:

1. Context size  
2. Temperature  
3. Sampling (top-p, top-k, repeat penalty)  
4. Hardware throughput  

None of them work alone.

They amplify each other.

---

# Context — Accumulated Pressure

Context is the active window of tokens.

Everything inside it influences the next token.

Large context:

- Reinforces tone
- Reinforces repetition
- Reinforces escalation
- Builds continuity

Small context:

- Resets faster
- Feels cleaner
- Feels less persistent

Context does not create intensity.

It accumulates it.

---

# Temperature — Permission to Deviate

Temperature rescales probabilities.

Low temperature:

- Picks high-probability tokens
- Stable tone
- Predictable structure

High temperature:

- Allows lower-probability tokens
- More variation
- Higher instability

It does not add creativity.

It increases risk.

---

# Sampling — The Gatekeeper

After probabilities are calculated,
sampling decides what is allowed.

## top-k

Limits the selection to the top K tokens.

Lower K:
More rigid.
More repetitive.

Higher K:
More exploratory.

---

## top-p (nucleus sampling)

Selects tokens whose cumulative probability mass reaches P.

Lower P:
Focused.
Controlled.

Higher P:
Wider exploration.
Less restraint.

top-p is dynamic.
top-k is fixed.

Together, they shape the candidate pool.

---

## repeat penalty

Reduces probability of recently used tokens.

Too low:
Loops.

Too high:
Forced awkward phrasing.

This is subtle.
Most users leave it at default and never understand why repetition happens.

---

# Hardware — The Tempo Multiplier

GPU acceleration does not change probabilities.

It changes speed.

Speed changes perceived intensity.

On a slow CPU:

- Tokens arrive slowly
- Reinforcement builds slowly
- Drift feels delayed

On a strong GPU:

- Tokens arrive fast
- Context fills quickly
- Sampling effects compound rapidly

Same model.
Different tempo.
Different perceived behavior.

---

# The Interaction Most Users Miss

Large context + high temperature + high top-p:

= amplified instability.

Large context + low temperature + low top-p:

= stable long-form structure.

Small context + high temperature:

= chaotic bursts.

Now add hardware speed.

The faster the loop,
the faster patterns lock in.

You are not changing intelligence.

You are shaping a dynamic system.

---

# Why This Matters

Most users change:

- Model
- Temperature
- Context
- Sampling

All at once.

Then they judge the model.

They never isolate variables.

That’s not tuning.

That’s guessing.

---

If you understand this chapter,
you are no longer asking:

“Is this model uncensored?”

You are asking:

“What environment am I creating?”

Next:
System prompts — the invisible layer that quietly dominates everything.
