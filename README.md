# Automated Spaced Recall Study System

An AI-powered learning platform that transforms PDF notes into an adaptive, personalized study experience.

Instead of traditional flashcards with fixed questions, this system breaks study material into **atomic concepts**, generates **dynamic open-ended questions**, evaluates descriptive answers using AI, and schedules reviews using the **FSRS (Free Spaced Repetition Scheduler)** algorithm.

---

## Motivation

Most students rely on rereading or cramming, both of which are inefficient for long-term retention.

This project aims to solve three major problems:

- Lack of structured revision
- Poor understanding of actual knowledge gaps
- Inefficient review schedules

By combining cognitive science with modern LLMs, the platform focuses study time on concepts that matter most.

---

## Features

### PDF → Structured Knowledge

- Upload study notes as PDFs
- Automatic text extraction
- AI-generated hierarchical topic tree
- Atomic concept extraction
- Semantic chunking and embeddings

---

### Adaptive Question Generation

Instead of memorizing flashcards, every review generates a new descriptive question from the underlying concept.

- Open-ended questions
- Concept-focused recall
- Dynamic rephrasing
- Retrieval-Augmented Generation (RAG)

---

### AI Answer Evaluation

Users answer in natural language.

The system:

- compares answers against canonical content
- grades understanding using an LLM
- maps performance onto the Anki 1–4 grading scale
- allows manual grade override

---

### Personalized Spaced Repetition

Uses **FSRS v6** instead of SM-2.

Benefits include:

- personalized intervals
- adaptive scheduling
- fewer unnecessary reviews
- higher long-term retention

Review history is continuously logged and used to train user-specific scheduling parameters.

---

### Learning Dashboard

Includes:

- Deck overview
- Upcoming reviews timeline
- Retention statistics
- Performance analytics
- AI clarification chat
- Topic tree visualization

---

# Architecture

```
                    PDF Upload
                         │
                         ▼
               Text Extraction
                         │
                         ▼
          Semantic Chunking + Embeddings
                         │
                         ▼
            AI Topic Extraction
                         │
                         ▼
            Hierarchical Topic Tree
                         │
                         ▼
             Atomic Knowledge Units
                         │
            ┌────────────┴────────────┐
            ▼                         ▼
     Question Generation       FSRS Scheduler
            │                         │
            ▼                         ▼
     Student Answer          Review Scheduling
            │
            ▼
      AI Rubric Evaluation
            │
            ▼
      Mastery Update
```

---

# Tech Stack

### Frontend

- Next.js
- React
- TypeScript

### Backend

- Next.js API Routes
- LangChain

### AI

- Gemini Flash 2.5
- OpenAI Embeddings
- Retrieval-Augmented Generation (RAG)

### Database

- Supabase
- pgvector

### Scheduling

- FSRS v6
- User-specific parameter training

### Visualization

- D3.js

---

# Learning Pipeline

1. Upload PDF notes.
2. Split notes into semantic chunks.
3. Generate embeddings.
4. Build a hierarchical topic tree.
5. Decompose into atomic concepts.
6. Generate descriptive questions.
7. User submits free-form answers.
8. AI evaluates conceptual understanding.
9. FSRS schedules the next review.
10. Repeat until mastery.

---

# Why Atomic Concepts?

Traditional flashcards often combine multiple ideas into a single card.

This project instead uses **immutable atomic concepts**, where every review targets one independently assessable piece of knowledge.

This improves:

- scheduling accuracy
- evaluation quality
- concept tracking
- mastery estimation

---

# Example Workflow

```text
Upload PDF
      ↓
Generate Topic Tree
      ↓
Create Atomic Concepts
      ↓
Generate Question
      ↓
User Answers
      ↓
AI Grades Answer
      ↓
FSRS Updates Schedule
      ↓
Repeat Until Mastery
```

---

# Results

Compared to early prototypes using SM-2 and static questions, the final system demonstrated:

- fewer unnecessary reviews
- better long-term retention
- adaptive scheduling
- higher quality assessment through descriptive answers
- improved alignment with cognitive science principles

---

# Future Improvements

- Image understanding
- Video lecture ingestion
- Collaborative study decks
- Multi-document knowledge graphs
- Better personalization through reinforcement learning
- Mobile application
- Offline review mode

---

# Project Structure

```
app/
components/
lib/
api/
database/
fsrs/
rag/
embeddings/
question-generation/
evaluation/
```

---

# Research Foundation

This project builds upon research in:

- Spaced Repetition
- Retrieval Practice
- FSRS
- Retrieval-Augmented Generation
- Knowledge Tracing
- Adaptive Learning
- Large Language Models in Education

---

# Authors

Developed as part of the **Experiential Learning (ACY 2025–26)** program at **RV College of Engineering**.

Team Members:

- Vivaan Hooda
- Sujal B
- Suraj Vaidyanathan
- Bivin Bheemaiah N K
- Disha M Bhat

---
