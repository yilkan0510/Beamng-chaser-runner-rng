# Chase Roulette for BeamNG.drive

Rolls a random BeamNG.drive car for the runner and a slightly quicker one for the chaser. It picks from every factory config in the game (version 0.39). You can open a lobby so a friend sees the same rolls, rules and countdown on their screen.

## Put it on GitHub Pages

1. Make a new public repository and upload `index.html` (and this README) to it.
2. In the repo, go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, then pick `main` and `/ (root)`, and save.
3. After a minute your site is live at `https://<your-username>.github.io/<repo-name>/`.

## Lobbies

- One person clicks **Create lobby** and gets a 4-character code.
- The other person types the code and clicks **Join**, or opens the invite link (`…/?lobby=CODE`).
- After that, rolls, rules, player names, the runner lock and the countdown sync between everyone in the lobby.

How it works: there's no server of your own. Browsers connect to each other directly (WebRTC) using the free public servers that come with [PeerJS](https://peerjs.com). They only help the two browsers find each other. On some strict networks, like school or work Wi-Fi, a direct connection can fail; it then falls back to PeerJS's free relay servers. If the lobby says it can't reach the server, try again or switch networks.

The person who created the lobby hosts it. If they close the tab, the lobby ends.

## Data

Stats are BeamNG's own figures from the official vehicle docs: https://docs.beamng.com/official_content/vehicles/
