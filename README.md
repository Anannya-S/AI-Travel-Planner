# AI Travel Planner

An AI-powered travel planning assistant built using **LangGraph**, **LLMs**, and **RAG**, capable of:
- Generating **day-wise itineraries**
- Selecting **budget-friendly flights & hotels**
- Ranking tourist spots based on **user interests**
- Exporting the final plan as a **structured PDF**

---

## Features
- **Natural language query parsing:** Converts user naturall language requests into structured JSON.
- **Flight selection:** Picks the cheapest available flight from dataset.
- **Hotel selection:** Chooses the best hotel while ensuring at least 25% of budget remains for sightseeing.
- **RAG-based Tourist spot ranking:** Uses vector similarity search (RAG) on places dataset to prioritize attractions based on user interests.
- **Dynamic itinerary building:** Considers opening hours, ticket costs, travel time, and daily limits.
- **Budget tracking:** Calculates transit + ticket expenses and outputs leftover budget.
- **Export as PDF:** Nicely formatted final itinerary with flight, hotel, and day-wise schedule.

---

## Tech Stack
- **LangGraph** for workflow orchestration
- **LLM** query parsing + text generation  
- **Vector Search (FAISS) + RAG** ranking tourist attractions  
- **Python(PyTorch, NumPy, JSON)** for backend logic  
- **ReportLab** for PDF generation  
- Custom **JSON datasets** (flights, hotels, places)

---

## Workflow
1. **User Input:** Natural language request (e.g., “Plan a 3-day trip to Paris under $2000 with history & food”).
2. **LLM Parsing:** Extracts structured fields (destination, budget, days, interests).  
3. **Flight & Hotel Selection:** Cheapest flight + best hotel within budget constraints.  
4. **RAG-based Ranking:** Retrieves tourist spots aligned with user interests.  
5. **Itinerary Builder:** Schedules places day-wise, respecting time, cost, and budget constraints.
6. **Final Output:** Generates a human-readable itinerary and exports it as a nicely formatted PDF.


