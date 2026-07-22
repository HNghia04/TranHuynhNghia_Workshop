---
title: "Week 9 Worklog"
date: 2026-06-30
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

## Week 9 Objectives

* Integrate WebSocket communication into the Game Client.
* Connect players to the Game Server after successful matchmaking.
* Implement the Game Session management mechanism.
* Synchronize game state among multiple players.
* Handle player disconnection and reconnection scenarios.

## Tasks Performed

| Day | Task | Start Date | Completion Date | Reference |
| --- | --- | --- | --- | --- |
| Tuesday | Integrated the sign-in functionality into the Game Client and implemented JWT token storage. | 30/06/2026 | 30/06/2026 | Amazon Cognito Documentation |
| Wednesday | Integrated the Matchmaking API and processed the response containing the Match ID, Game Server IP address, and port number. | 01/07/2026 | 01/07/2026 | Amazon API Gateway Documentation |
| Thursday | Implemented the Game Client functionality to establish a WebSocket connection with the Game Server after successful matchmaking. | 02/07/2026 | 02/07/2026 | WebSocket Client Documentation |
| Friday | Designed the WebSocket message format for Join Room, Player Update, Game Event, and Disconnect operations. | 03/07/2026 | 03/07/2026 | Protocol Design Documentation |
| Saturday | Implemented the player state synchronization mechanism among multiple clients within the same Game Session. | 04/07/2026 | 04/07/2026 | Project Source Code |
| Sunday | Implemented the reconnection mechanism and verified whether disconnected players still belonged to their Game Session. | 05/07/2026 | 05/07/2026 | Testing Notes |
| Monday | Performed end-to-end testing, covering authentication, matchmaking, Game Server connection, and real-time state synchronization. | 06/07/2026 | 06/07/2026 | Amazon CloudWatch Logs and Testing Reports |

## Achievements

* Successfully integrated Amazon Cognito into the Game Client.

* The Game Client is capable of:

  * User Sign-in
  * Receiving JWT Tokens
  * Sending Matchmaking Requests
  * Receiving Game Session Information
  * Connecting to the Game Server

* Designed a standardized WebSocket message structure, including:

  * JoinRoom
  * PlayerJoined
  * PlayerStateUpdate
  * GameEvent
  * MatchStarted
  * MatchEnded
  * PlayerDisconnected

* Successfully synchronized game state among multiple players within the same Game Session.

* Implemented Game Server validation using Match ID and Player ID when players join a game room.

* Developed mechanisms to handle:

  * Player Disconnection
  * Player Reconnection
  * Player Leaving the Match
  * Full Game Room Detection
  * Match Completion

* Successfully completed the end-to-end gameplay workflow, including:

  * Authentication
  * Matchmaking
  * Session Allocation
  * WebSocket Connection
  * Real-time Synchronization
  * Match Completion