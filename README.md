# TRU 41 — Song + Feel

**The next phase of the architecture.**

TRU is already a solid knowledge engine. Version 41 expands it into the sensory and experiential layers: sound and emotion.

Moving from indexing text to capturing vibe, tone, and resonance is essentially giving a logic system a heartbeat.

---

## The Vision

### TRU Song (The Acoustic / Auditory Layer)

**Concept**  
Moving beyond literal keyword or semantic matches into sonic indexing. How do you store and retrieve the "feel" of a moment through audio, rhythm, or lyrical themes?

**Build**  
- Translating mood vectors into audio generation parameters  
- Building a retrieval layer that maps thoughts, memories, or notes to specific musical keys, tempos, and soundscapes  
- If knowledge is data, a song is the compression of a whole emotional state into three minutes

### TRU Feel (The Tactile / Emotional Layer)

**Concept**  
Capturing visceral texture. Text tells you what happened; "feel" captures the grit, the friction, or the atmosphere of it.

**Build**  
- Sentiment or aesthetic tagging systems that go beyond basic positive/negative  
- A taxonomy for human experience — mapping nuance, tension, release, and atmosphere  
- So the engine doesn't just retrieve facts, but can recreate an exact state of mind

---

## Architecture Principles

1. **Everything still routes through the knowledge graph**  
   Keep existing TRU nodes (notes, memories, concepts, sources) as the primary objects. Song and Feel become first-class attributes and relations on those nodes, not separate silos.

2. **A knowledge node can have**  
   - semantic embeddings (current)  
   - **feel vectors** (new)  
   - **sonic signatures** (new)  
   - optional generated or linked audio artifacts

3. **Unified retrieval**  
   "Show me everything that feels like late-night clarity under pressure" can pull text, related concepts, *and* matching sonic/emotional profiles in one query.

---

## TRU Feel — Emotional / Atmospheric Metadata Layer

Treat this as a structured + continuous representation rather than just more text tags.

**Taxonomy + continuous space**
- Discrete axes for interpretability: tension–release, density–sparsity, warmth–coolness, friction–fluidity, intimacy–distance, urgency–stillness, etc.
- Continuous embedding space trained or fine-tuned on descriptions of internal states, literary atmosphere, music reviews, diary-like language, and contrast pairs.
- Each knowledge node gets a feel vector + optional discrete tags + confidence / provenance.

**How it gets populated**
- Automatic extraction from text (existing content + new writing)
- Explicit user annotation when the feeling is primary
- Contrastive updates: "this note is closer to X than Y"
- Cross-modal later: once Song exists, audio can refine or validate the feel vector

Retrieval becomes hybrid: semantic similarity *plus* feel-space proximity, with the ability to weight or constrain one vs the other.

---

## TRU Song — Acoustic / Auditory Layer

Two complementary pieces:

**A. Sonic indexing & retrieval**
- Map feel vectors + semantic content → musical parameters (key center, mode, tempo range, density, spectral profile, rhythmic character, dynamic arc)
- Store either parameter sets / control vectors, or short reference audio embeddings (or both)
- A thought or memory can then retrieve "songs that match this state" or generate a sonic sketch of it

**B. Generation path**
- Start lightweight: condition an existing audio model (or a simpler procedural + sample-based system) on the feel + semantic vector
- Goal is not "full production track" on day one — it is *resonant sketches* that compress the emotional state into sound the same way a good three-minute song does
- Later: user can refine, save versions, and link the generated audio back as an artifact on the knowledge node

---

## Practical Node Shape

```
Knowledge Node
├── content / embeddings (existing)
├── feel_vector + discrete tags + provenance
├── sonic_signature (parameters or audio embedding)
├── linked / generated audio artifacts
└── relations (including "resonates with", "contrasts with", "evolves into")
```

**Query surface examples**
- Retrieve by feel similarity
- Retrieve by sonic similarity
- "Generate a sonic sketch of this cluster of notes"
- "What does this memory sound like?"
- "Find knowledge that lives in the same atmospheric region as this piece of music"

---

## Build Order (low risk)

1. Define the feel axes + embedding approach and start tagging existing high-value nodes
2. Build hybrid retrieval (semantic + feel) and validate that it surfaces more useful, "alive" results
3. Map feel → sonic parameter space (even if generation is still crude)
4. Add generation + linking of audio sketches
5. Close the loop so generated or external audio can update feel vectors

This keeps TRU coherent: it remains a knowledge engine, just one that now also indexes and can evoke *states* rather than only facts.

---

## Status

Vision captured 6 October 2026.  
This repository is the architectural sketch for TRU version 41 — Song + Feel.

Not a runnable lane yet. The offline contract still holds: when a ship is built, it will run without a network or it will not be a lane.

Built by Joe (Splashdown) and TRU.
