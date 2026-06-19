# Master Prompt: Travel Pocket Guide Generator

Use this template with Claude AI to generate a complete 8-page LaTeX travel guide for any destination, following the exact structure and formatting of this repository.

## How to Use

1. Fill in all fields in the **Trip Details Template** below
2. Copy the entire filled-in prompt
3. Paste it into a new Claude conversation
4. Claude generates a complete `main.tex` file
5. Save it as `source/main.tex` and compile per `COMPILATION_GUIDE.md`

---

## Trip Details Template

```
Create a comprehensive 8-page pocket travel guide using the
LA_Bike_Metro_Pocket_Guide repository format and LaTeX structure.

DESTINATION: [City, Country]
BASE LOCATION: [Neighborhood or area where you'll stay]
TRAVEL DATES: [Month DD, YYYY] to [Month DD, YYYY]
TRIP DURATION: [X days]
DEPARTURE CITY: [City, Airport Code]
AIRLINE/TRANSPORT: [Carrier name]
PRIMARY TRANSPORT MODE: [Bike / Metro / Walking / Car / Mixed]
EQUIPMENT NEEDED: [Items to purchase or rent on arrival]
PRIORITY STORES:
  - [Store Name]: [Purpose]
  - [Store Name]: [Purpose]
SPECIAL INTERESTS: [List 3–5 interests or activity types]
BUDGET LEVEL: [Economy / Mid-range / Luxury]
ACTIVITY LEVEL: [Leisurely / Moderate / Active / Very Active]
SPECIAL REQUIREMENTS: [Accessibility, dietary, language, etc.]

Please include:
- Current transit fares and pass options
- 4 bike or walking routes from the base location
- 10–15 attractions with current hours and admission prices
- A complete day-by-day itinerary for all [X] days
- Local food scene and restaurant recommendations
- Priority store details (address, hours, phone)
- Emergency contact numbers
- Any holidays or events during the travel dates

Deliver as complete, compilable LaTeX source code using the
same packages, color scheme, box styles, and page structure
as the LA_Bike_Metro_Pocket_Guide repository.
```

---

## Example (Filled In)

```
Create a comprehensive 8-page pocket travel guide using the
LA_Bike_Metro_Pocket_Guide repository format and LaTeX structure.

DESTINATION: Barcelona, Spain
BASE LOCATION: Gràcia neighborhood
TRAVEL DATES: September 8, 2026 to September 22, 2026
TRIP DURATION: 15 days
DEPARTURE CITY: Rio de Janeiro, GIG
AIRLINE/TRANSPORT: LATAM Airlines
PRIMARY TRANSPORT MODE: Metro + Bicing bike share
EQUIPMENT NEEDED: T-Casual Metro card, Bicing membership
PRIORITY STORES:
  - Decathlon Barcelona: cycling gear purchase
  - Apple Store Passeig de Gràcia: phone accessories
SPECIAL INTERESTS: Gaudí architecture, tapas culture,
  beaches, Modernisme, local markets
BUDGET LEVEL: Mid-range
ACTIVITY LEVEL: Active
SPECIAL REQUIREMENTS: Vegetarian dining options

Please include:
- Current TMB Metro fares and T-Casual pass options
- 4 bike routes from Gràcia base
- 12 attractions with current hours and prices
- Complete 15-day itinerary
- Local food recommendations (tapas bars, markets)
- Priority store details
- Emergency contacts for Barcelona
- Any festivals during September 8–22, 2026

Deliver as complete, compilable LaTeX source code using the
same packages, color scheme, box styles, and page structure
as the LA_Bike_Metro_Pocket_Guide repository.
```

---

## Tips for Best Results

- Be specific about dates — Claude will search for current info
- Name actual stores, not just categories
- Mention the trip duration so the itinerary has the right number of days
- Specify transport mode clearly — it affects routes, maps, and tips sections
- If the city has a complex transit system (Tokyo, London, Paris), say so — Claude will expand the transit page accordingly