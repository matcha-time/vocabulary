# Vocabulary Flashcards

A simple repository to organize and share vocabulary flashcards by language, topic, and learning roadmaps.

---

## What's inside

- Languages organized at the top level (e.g., `french`, `english`, `spanish`, `korean`).
- Within each language:
  - `topics/` for curated sets (e.g., time, body, health, numbers).
  - `roadmaps/` for progressive decks aligned to courses, exams or everyday life.
  - `shared/` for common utilities or references (e.g., parts of speech, frequency lists).

Example structure:

```
/
├─ english/
│  ├─ topics/
│  │  ├─ time.json
│  │  ├─ body.json
│  │  └─ numbers.json
│  ├─ roadmaps/
│  │  ├─ level-a1.json
│  │  ├─ level-a2.json
│  │  └─ level-b1.json
│  └─ shared/
│     └─ core-2000.json
├─ spanish/
│  └─ topics/
│     └─ health.json
└─ korean/
   └─ roadmaps/
      └─ topik-1.json
```

---

## Flashcard format

All decks are simple JSON arrays of cards. Keep files UTF-8 encoded.

```json
[
  {
    "term": "apple",
    "translation": "la manzana",
    "language": "english",
    "topic": "food",
    "examples": [
      { "source": "I eat an apple every day.", "translation": "Como una manzana todos los días." }
    ],
    "tags": ["A1", "noun"],
  }
]
```

Required fields:
- `term`: the headword in the deck language
- `translation`: meaning in the target/paired language
    **For languages with articles (e.g., Spanish, French), include the article with the noun**, e.g., `"term": "la manzana"`

Optional but recommended:
- `notes`, `examples[]`, `tags[]`, `topic`

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

Roadmaps are progressive decks (A1→C1, TOPIK 1→6, etc.). Each file should represent one stage and build on the previous, no duplicate entries (e.g., A2 does not contain A1).

---

## License

Unless stated otherwise inside a deck, content is contributed under the MIT License. If your deck uses third-party sources, cite them in the deck metadata.
