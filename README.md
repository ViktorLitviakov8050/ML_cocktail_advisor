# Cocktail Advisor Chat

A Python-based chat application that uses RAG (Retrieval-Augmented Generation) to provide cocktail recommendations and answer cocktail-related questions.

## Features

- Chat interface for cocktail-related queries
- Integration with OpenAI GPT for natural language processing
- Vector database (FAISS) for storing and retrieving cocktail information
- User preference tracking for personalized recommendations
- RAG system for enhanced responses
- Optional favorites system for tracking preferred ingredients

## Prerequisites

- Python 3.8+
- OpenAI API key

## Installation

1. Clone the repository:

```bash
git clone https://github.com/ViktorLitviakov8050/cocktail-advisor.git
cd cocktail-advisor
```

2. Set up environment variables in `.env`:
```env
OPENAI_API_KEY=your_key_here
ENABLE_FAVORITES=true  # or false to disable favorites
```

## Running the Application

You can control the favorites functionality when starting the app:

```bash
# Run with favorites (if ENABLE_FAVORITES=true in .env)
uvicorn app.main:app --reload

# Override .env and run without favorites
ENABLE_FAVORITES=false uvicorn app.main:app --reload
```

Questions for stakeholders:
- Should be implemented favorite ingredients section on UI side or no? (probably it's a good option to change time by time your favorite ingredients)
- Should favorites persist between sessions or reset on each startup?
- Should we limit the number of favorite ingredients a user can save?
- Should favorite ingredients influence the ranking of cocktail recommendations?
- Should we add the ability to group favorite ingredients by category (e.g., spirits, mixers, garnishes)?