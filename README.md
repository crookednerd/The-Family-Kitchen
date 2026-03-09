# 🌿 The Family Kitchen  
  
A private family recipe website built with React — a searchable, filterable collection of 320+ recipes passed down through the family. Designed to be easy to use for everyone, including less tech-savvy family members.  
  
-----  
  
## ✨ Features  
  
- **320+ real family recipes** parsed from the original Google Drive collection  
- **Search** by recipe name, family member, or ingredient  
- **Filter by category** — 29 categories including Soups, Cookies, Poutines, Poultry, Perogy Fillings, Musketeers Collection, and more  
- **Recipe cards** with hand-drawn SVG illustrations unique to each food category  
- **Full recipe modal** with ingredients, step-by-step instructions, and notes  
- **Mobile-first design** — 2-column grid on mobile, scales up to 4 columns on desktop  
- **Family attribution** — recipes credited to Aunty Caroline, Aunty Donna, Kyra, Erykah, Crystal, Marco, Natylee, and more  
  
-----  
  
## 🗂️ Recipe Categories  
  
|Category          |Category           |Category             |  
|------------------|-------------------|---------------------|  
|Breakfast         |Soups              |Beef                 |  
|Baking            |Salads             |Pork                 |  
|Cookies           |Poultry            |Fish & Seafood       |  
|Squares & Bars    |Pizza              |Sandwiches           |  
|Cakes & Desserts  |Pasta              |Poutines             |  
|Pies & Tarts      |Rice Dishes        |Perogy Fillings      |  
|Sweets            |Dips & Appetizers  |Icings & Fillings    |  
|Breads & Doughs   |Drinks             |Healthy Options      |  
|Casseroles        |Sauces & Marinades |Holiday              |  
|Vegetables & Sides|Canning & Preserves|Musketeers Collection|  
  
-----  
  
## 🚀 Getting Started  
  
### Prerequisites  
  
- [Node.js](https://nodejs.org/) v18+  
- npm or yarn  
  
### Installation  
  
```bash  
# Clone the repo  
git clone https://github.com/your-username/family-kitchen.git  
cd family-kitchen  
  
# Install dependencies  
npm install  
  
# Start the dev server  
npm run dev  
```  
  
The app will be running at `http://localhost:5173`.  
  
### Build for Production  
  
```bash  
npm run build  
```  
  
Output goes to the `/dist` folder, ready to deploy.  
  
-----  
  
## 🛠️ Tech Stack  
  
- **React 18** — UI framework  
- **Vite** — build tool and dev server  
- **DM Sans** (Google Fonts) — clean, readable sans-serif font  
- **Inline SVG illustrations** — hand-drawn line art, one per food category  
- **Pure CSS** — no UI library, all custom styles with CSS variables  
- No external component dependencies  
  
-----  
  
## 📁 Project Structure  
  
```  
family-kitchen/  
├── src/  
│   └── family-recipes.jsx   # Main app — all recipes + UI in one file  
├── public/  
│   └── index.html  
├── package.json  
└── README.md  
```  
  
All 320 recipes and the full UI live in a single `family-recipes.jsx` file. Recipes were parsed from the original `.docx` files exported from Google Drive and compiled into a JavaScript data array.  
  
-----  
  
## 📖 Adding New Recipes  
  
Find the `RECIPES` array in `family-recipes.jsx` and add a new entry following this structure:  
  
```js  
{  
  id: 321,                          // next sequential ID  
  emoji: '🍳',                      // fallback emoji (not displayed)  
  category: 'Breakfast',            // must match an existing category  
  title: "Grandma's French Toast",  
  author: 'Grandma',                // optional  
  ingredients: [  
    { amount: '2', name: 'Eggs' },  
    { amount: '1/4 cup', name: 'Milk' },  
    { amount: '2 slices', name: 'Thick bread' },  
  ],  
  steps: [  
    'Whisk eggs and milk together in a shallow bowl.',  
    'Dip bread slices in the egg mixture, coating both sides.',  
    'Cook in a buttered pan over medium heat until golden, about 2 minutes per side.',  
  ],  
}  
```  
  
To add a **new category**, also add entries to `CAT_PALETTES` (background + stroke colour) and `LINE_DRAWINGS` (SVG illustration) in the same file.  
  
-----  
  
## 🌐 Deployment  
  
This is a standard Vite + React app and can be deployed anywhere static files are hosted:  
  
- **Vercel** — connect your GitHub repo, zero config needed  
- **Netlify** — drag and drop the `/dist` folder or connect via Git  
- **GitHub Pages** — use the `gh-pages` package or GitHub Actions  
  
-----  
  
## 📸 Screenshots  
  
> *Add screenshots here once deployed*  
  
-----  
  
## 🤝 Contributing (Family Only)  
  
This is a private family project. If you’d like to add a recipe:  
  
1. Open an issue with the recipe details, or  
1. Fork the repo, add your recipe to the array, and open a pull request  
  
-----  
  
## 📜 License  
  
Private — for family use only. Not for public distribution.  
