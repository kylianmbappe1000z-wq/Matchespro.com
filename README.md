Deriv Digit-5 Matches Bot (demo)
=================================

This package contains an educational Node.js bot that connects to Deriv's WebSocket API (demo or real token),
collects recent ticks, runs a small ensemble of simple predictors and places a DIGITMATCH contract when the
ensemble confidence for digit `5` exceeds a configurable threshold.

IMPORTANT: This is an educational example. Test on a demo account only. Do NOT commit or share your API token.

Files:
- bot.js         : Main bot source (Node.js)
- package.json   : NPM package file
- .gitignore     : Ignore environment and node_modules
- README.md      : This file

How to use
----------
1. Install Node.js (v16+ recommended).
2. In the project folder, install dependencies:

   npm install

3. Create a `.env` file in the project root with your demo token:

   DERIV_TOKEN=your_demo_token_here

   Alternatively export DERIV_TOKEN in your shell:
   export DERIV_TOKEN="your_demo_token_here"

4. Run the bot in dry-run (no real buys):

   node bot.js --dry

5. Run the bot live (will place buys using your token — be careful):

   node bot.js

Security note
-------------
- Never share your live API tokens publicly.
- Rotate tokens if you suspect they were exposed.
- Use demo tokens while testing.

If you want extra features (backtester, ML model, UI, martingale persistence), ask and I will add them.
