# How to Add New Surveys

The fastest way to add surveys is to paste the raw chat text into Claude Code and let it handle the parsing.

## Steps

1. Copy the raw survey post(s) from your LINE/chat group
2. Open Claude Code in this project directory
3. Use the prompt below, then paste the chat text after it

## Prompt

```
Add new surveys to the `surveys` array in index.html. Parse the raw chat text below to extract each survey. For each one:
- Extract: title (English), person (nickname), program (e.g. YMBA, MBA ENG #19), description (1-2 sentence English summary), categories (from: food, beverage, health, lifestyle, consumer, finance, pets), time estimate, incentive, and the Google Forms link
- Generate Thai translations for title_th and desc_th
- Use Unicode escapes for Thai strings (e.g. \u0e41\u0e1a\u0e1a)
- Skip any survey whose link already exists in the array
- Add new entries before the closing `];`

Raw chat text:
```

Then paste the chat messages right after.

## Survey Data Format (for manual edits)

Each survey is a JS object in the `surveys` array inside `index.html`:

```js
{
  title: "English Title",
  title_th: "ชื่อภาษาไทย",
  person: "Nickname",
  program: "MBA ENG #19",
  desc: "English description of the survey topic.",
  desc_th: "คำอธิบายภาษาไทย",
  categories: ["food", "consumer"],  // pick from: food, beverage, health, lifestyle, consumer, finance, pets
  time: "5-10 min",                  // or null
  incentive: "Starbucks 200 THB x5", // or null
  link: "https://forms.gle/..."
}
```

Add new entries anywhere in the `surveys` array (before the closing `];`).
