# TeddyTalk

TeddyTalk is a small browser video-call and conference app. It supports up to 8 people in a room, with browser-to-browser WebRTC audio/video and room chat. The Node server only serves the page and relays call setup messages; media streams are exchanged peer to peer.

## Run locally

1. Install Node.js 18 or newer.
2. In this folder, run `npm install` once.
3. Run `npm start` and open `http://localhost:3000`.
4. Start a call, copy the room link, then open it in another browser/device and press **Join live call**.

Camera and microphone access works on localhost. For people outside your network, host the app on an HTTPS site and use a TURN server for networks that block direct peer connections. The included signaling server uses WebSocket; terminate HTTPS/WSS at the hosting provider or reverse proxy. Calls are limited to 8 participants and use a mesh connection, so performance depends on each participant's network and device.
