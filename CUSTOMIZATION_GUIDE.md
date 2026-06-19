# Customization Guide

How to modify `source/main.tex` for your own trip, or create a guide for a different destination.

## Quick Edits (5 minutes)

### Change Travel Dates
Find and replace in `source/main.tex`:
```
November 10--26, 2025
```

### Change City and Location Names
Search for and replace:
- `Los Angeles` → your destination city
- `Alhambra` → your base neighborhood
- `LAX` → your arrival airport code
- `GIG` → your departure airport code

### Update Emergency Contacts
Find the `Emergency Contacts` section (Page 2) and replace phone numbers and service names.

### Edit an Attraction
Each attraction uses this structure:
```latex
\begin{infobox}[colback=gray!10,colframe=gray]
\textbf{Attraction Name}\\
\faMapMarker\ Address (distance from base)\\
\faDollarSign\ Price | \faClock\ Hours\\
One-line description.
\end{infobox}
```

---

## Moderate Changes (15–30 minutes)

### Change the Color Scheme

Find near the top of `source/main.tex`:
```latex
\definecolor{primary}{RGB}{25,118,210}
\definecolor{secondary}{RGB}{79,195,247}
\definecolor{accent}{RGB}{41,182,246}
\definecolor{warning}{RGB}{255,152,0}
\definecolor{success}{RGB}{76,175,80}
\definecolor{danger}{RGB}{244,67,54}
```

Replace RGB values with your preferred colors. Use [htmlcolorcodes.com](https://htmlcolorcodes.com/) to find RGB codes.

### Remove a Section
Find the section heading and delete from it to the next `\section*`, `\subsection*`, or `\newpage`.

### Add a New Section
```latex
\subsection*{\faIcon\ Section Title}

\begin{infobox}
Your content here.
\end{infobox}
```

---

## Create a Guide for a Different Destination

### Using Claude AI (Recommended)

1. Open `MASTER_PROMPT.md`
2. Fill in all the trip detail fields
3. Paste the complete prompt into Claude
4. Claude generates a full LaTeX source file
5. Save it as `source/main.tex`
6. Compile using `COMPILATION_GUIDE.md`

### Manual Customization

Replace all destination-specific content in each page:

| Page | What to Update |
|------|---------------|
| 2 | Flight details, emergency contacts, weather |
| 3 | Transit system names, lines, fares, apps |
| 4 | Local bike routes and distances |
| 5 | Attractions with hours and prices |
| 6 | Shopping locations, practical tips |
| 7 | Daily itinerary (adjust number of days) |
| 8 | Emergency numbers, addresses, websites |

---

## Advanced Tweaks

### Change Font Sizes
```latex
\titleformat{\section}
  {\Large\bfseries\color{primary}}  % Change \Large here
```
Options: `\small`, `\normalsize`, `\large`, `\Large`, `\LARGE`, `\huge`, `\Huge`

### Add a Hyperlink
```latex
\href{https://example.com}{Link Text}
```

### Adjust Number of Itinerary Days
On Page 7, add or remove `tcolorbox` day blocks:
```latex
\begin{tcolorbox}[colback=primary!5,colframe=primary!50,title=\textbf{Day X - DOW, Date: THEME}]
Morning activity → Afternoon activity\\
Evening notes
\end{tcolorbox}
```