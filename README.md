# Vocabulary Flashcards

A simple repository to organize and share vocabulary flashcards by language, topic, and learning roadmap.

---

## What's inside

- Languages organized at the top level (e.g., `english`, `spanish`, `japanese`).
- Within each language:
  - `topics/` for curated sets (e.g., food, travel, business, tech).
  - `roadmaps/` for progressive decks aligned to study plans or courses.
  - `shared/` for common utilities or references (e.g., parts of speech, frequency lists).

Example structure:

```
/
├─ english/
│  ├─ topics/
│  │  ├─ food.json
│  │  ├─ travel.json
│  │  └─ business.json
│  ├─ roadmaps/
│  │  ├─ a1.json
│  │  ├─ a2.json
│  │  └─ b1.json
│  └─ shared/
│     └─ core-100.json
├─ spanish/
│  └─ topics/
│     └─ salud.json
└─ japanese/
   └─ roadmaps/
      └─ n5.json
```

---

## Flashcard format

All decks are simple JSON arrays of cards. Keep files UTF-8 encoded.

```json
[
  {
    "term": "apple",
    "translation": "manzana",
    "language": "english",
    "topic": "food",
    "notes": "countable; common beginner noun",
    "examples": [
      { "source": "I eat an apple every day.", "translation": "Como una manzana todos los días." }
    ],
    "tags": ["A1", "noun"],
    "createdAt": "2025-11-04"
  }
]
```

Required fields:
- `term`: the headword in the deck language
- `translation`: meaning in the target/paired language

Optional but recommended:
- `notes`, `examples[]`, `tags[]`, `topic`, `createdAt`

You may also add per-deck metadata via a sibling file named like `food.meta.json`:

```json
{
  "title": "Food Basics",
  "language": "english",
  "description": "Core food vocabulary for beginners",
  "level": "A1",
  "source": "Community curated"
}
```

---

## Contributing

- Add new decks under the correct language and folder (`topics/` or `roadmaps/`).
- Use lowercase filenames with hyphens, e.g., `phrasal-verbs.json`.
- Validate JSON (no comments) and keep consistent fields.
- Prefer small, focused decks (50–150 cards) over huge files.
- Include at least 1 usage example when possible.

### PR checklist
- Deck placed in the right language and category
- JSON is valid and UTF-8 encoded
- Contains `term` and `translation` for every card
- No duplicate `term` entries within the same deck

---

## Roadmaps

Roadmaps are progressive decks (A1→C1, JLPT N5→N1, etc.). Each file should represent one stage and build on the previous. Keep difficulty and scope consistent within each stage.

---

## License

Unless stated otherwise inside a deck, content is contributed under the MIT License. If your deck uses third-party sources, cite them in the deck metadata.
