 # Maritime Coordinator Agent

This is an uncertainty-driven agentic framework for maritime situational awareness. 
A central Coordinator Agent that dynamically orchestrates perception, contextualization,
reasoning, and action selection. It includes Qwen2-VL for semantic verification only when the expected value of information justifies the cost.

## Overview

Conventional maritime AI pipelines run a fixed sequence of models on every frame.
This framework instead:

1. **Perceives** the scene with a maritime object detector.
2. **Contextualizes** each detection with AIS, weather, history, and domain knowledge.
3. **Quantifies uncertainty** from detector confidence, modal disagreement, and
   contextual inconsistency.
4. **Selects an action** — `Accept`, `Verify`, or `Acquire additional information` —
   using threshold rules and Expected Value of Information (EVI).
5. **Reasons semantically** with Qwen2-VL when verification is required.

The agent balances decision utility, computational cost, and operational risk.

