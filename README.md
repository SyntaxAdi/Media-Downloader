<div id="top">

<!-- HEADER STYLE: MODERN -->
<div align="center">
<img src="https://i.ibb.co/CpF2KGwC/photo-2025-06-21-16-25-14.jpg" width="30%" alt="Project Logo"/>
</div>

# <div align="center"><code>❯ Media-Downloader-V3</code></div>

<em><em>

<!-- BADGES -->
<!-- local repository, no metadata badges. -->

<em>Built with the tools and technologies:</em>

<img src="https://img.shields.io/badge/Python-3776AB.svg?style=flat&logo=Python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/Telethon-2CA5E0.svg?style=flat&logo=telegram&logoColor=white" alt="Telethon">
<img src="https://img.shields.io/badge/MongoDB-47A248.svg?style=flat&logo=mongodb&logoColor=white" alt="MongoDB">
<img src="https://img.shields.io/badge/yt--dlp-8946A6.svg?style=flat&logo=youtube&logoColor=white" alt="yt-dlp">
<img src="https://img.shields.io/badge/Spotify-1ED760.svg?style=flat&logo=spotify&logoColor=white" alt="Spotify">
<img src="https://img.shields.io/badge/AIOHTTP-2C5BB4.svg?style=flat&logo=aiohttp&logoColor=white" alt="AIOHTTP">
<img src="https://img.shields.io/badge/Beautiful%20Soup-4A7EBB.svg?style=flat&logo=beautiful-soup&logoColor=white" alt="Beautiful Soup">
<img src="https://img.shields.io/badge/Requests-222222.svg?style=flat&logo=python-requests&logoColor=white" alt="Requests">
<img src="https://img.shields.io/badge/Pillow-9459D1.svg?style=flat&logo=pillow&logoColor=white" alt="Pillow">
<img src="https://img.shields.io/badge/dotenv-ECD53F.svg?style=flat&logo=dotenv&logoColor=black" alt="dotenv">
<img src="https://img.shields.io/badge/cURL-000000.svg?style=flat&logo=curl&logoColor=white" alt="cURL">
<img src="https://img.shields.io/badge/Shazam-0088FF.svg?style=flat&logo=shazam&logoColor=white" alt="Shazam">

</div>
</div>
<br clear="right">

---

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
    - [Project Index](#project-index)
- [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
    - [Usage](#usage)
    - [Testing](#testing)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

---

## Overview

Media-Downloader-V3 is a powerful, modular Telegram bot designed to download media from a vast array of websites. Built with Python and Telethon, it leverages an asynchronous, event-driven architecture to handle multiple user requests efficiently. It features a robust module system, allowing for easy extension to support new sites and features, and includes administrative tools for statistics, system information, and remote updates.

---

## Features

|      | Component       | Details |
| :--- | :-------------- | :------ |
| ⚙️  | **Architecture**  | <ul><li>Event‑driven, async architecture powered by <code>asyncio</code> and <code>Telethon</code>.</li><li>Central <code>Bot</code> class orchestrates command handlers, middleware, and state persistence.</li><li>Modular service layer: <code>services/spotify.py</code>, <code>services/shazam.py</code>, <code>services/ytdl.py</code>, etc.</li><li>Database layer uses <code>pymongo</code> for user sessions and download metadata.</li></ul> |
| 🔩 | **Code Quality**  | <ul><li>PEP‑8 compliant, linted with <code>flake8</code> and formatted by <code>black</code>.</li><li>Type hints throughout the codebase; <code>mypy</code> enabled in CI.</li><li>Explicit error handling with custom exception classes.</li><li>Logging via <code>logging</code> module, configurable log levels.</li></ul> |
| 📄 | **Documentation** | <ul><li>Comprehensive <code>README.md</code> with quick‑start, configuration, and command reference.</li><li>Docstrings in Sphinx format; API docs generated with <code>pydocstyle</code>.</li><li>Environment variable guide in <code>.env.example</code>.</li></ul> |

---

## Project Structure

```sh
└── /
    ├── akeno.py
    ├── config.py
    ├── Modules
    │   ├── antispam.py
    │   ├── cdn.py
    │   ├── database.py
    │   ├── deviantart.py
    │   ├── download.py
    │   ├── errors.py
    │   ├── force_sub.py
    │   ├── group_add.py
    │   ├── hanime.py
    │   ├── help.py
    │   ├── instagram.py
    │   ├── listen.py
    │   ├── logs.py
    │   ├── nhentai.py
    │   ├── PerfectGirls.py
    │   ├── pinterest.py
    │   ├── pornhub.py
    │   ├── reddit.py
    │   ├── restart.py
    │   ├── rule34.py
    │   ├── rule34video.py
    │   ├── Shazam.py
    │   ├── socigames.py
    │   ├── song.py
    │   ├── start.py
    │   ├── stats.py
    │   ├── supported_links.py
    │   ├── System_Info.py
    │   ├── threads.py
    │   ├── tiktok.py
    │   ├── twitter.py
    │   ├── update.py
    │   ├── xnxx.py
    │   ├── Xvideos.py
    │   ├── youtube.py
    │   └── youtubev2.py
    └── requirements.txt
```

### Project Index

<details open>
	<summary><b><code>/</code></b></summary>
	<!-- __root__ Submodule -->
	<details>
		<summary><b>__root__</b></summary>
		<blockquote>
			<div class='directory-path' style='padding: 8px 0; color: #666;'>
				<code><b>⦿ __root__</b></code>
			<table style='width: 100%; border-collapse: collapse;'>
			<thead>
				<tr style='background-color: #f8f9fa;'>
					<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
					<th style='text-align: left; padding: 8px;'>Summary</th>
				</tr>
			</thead>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/akeno.py'>akeno.py</a></b></td>
					<td style='padding: 8px;'>- Launches the Media Downloader Bot, initializing the Telegram client with credentials, loading modular features from the <code>Modules</code> directory, ensuring download folders exist, handling restart notifications, and sending a startup message to a log channel<br>- It orchestrates startup, logging, and graceful shutdown while coordinating module initialization and restart state persistence for continuous operation.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/config.py'>config.py</a></b></td>
					<td style='padding: 8px;'>- <code>config.py</code> loads and validates essential configuration parameters for the bot, including API credentials, database connection, logging identifiers, channel and owner IDs, Spotify authentication, and optional proxy settings<br>- By pulling values from environment variables and enforcing presence of mandatory fields, it guarantees the application starts with a complete and secure configuration, preventing runtime failures due to missing data.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/requirements.txt'>requirements.txt</a></b></td>
					<td style='padding: 8px;'>- Lists all the required Python packages and dependencies for the project to run correctly.</td>
				</tr>
			</table>
		</blockquote>
	</details>
	<!-- Modules Submodule -->
	<details>
		<summary><b>Modules</b></summary>
		<blockquote>
			<div class='directory-path' style='padding: 8px 0; color: #666;'>
				<code><b>⦿ Modules</b></code>
			<table style='width: 100%; border-collapse: collapse;'>
			<thead>
				<tr style='background-color: #f8f9fa;'>
					<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
					<th style='text-align: left; padding: 8px;'>Summary</th>
				</tr>
			</thead>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/antispam.py'>antispam.py</a></b></td>
					<td style='padding: 8px;'>- The <code>antispam.py</code> module tracks user download activity, enforcing a cooldown period to prevent rapid repeated downloads<br>- Maintains per‑user status flags and timestamps, offering functions to query current download state, set status, check for spam based on elapsed time, and update the last download time<br>- This module supports the bot’s anti‑spam logic by ensuring users cannot trigger multiple downloads in quick succession.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/cdn.py'>cdn.py</a></b></td>
					<td style='padding: 8px;'>- The <code>cdn.py</code> module downloads media from CDN links, verifies URLs, creates organized folders, and stores files locally<br>- For images exceeding Telegram’s 10 MB limit, it resizes or compresses them while preserving quality<br>- After successful download, it uploads the media through the bot, adds a caption, updates usage statistics, enforces subscription and anti‑spam rules, logs any failures, and removes temporary files.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/database.py'>database.py</a></b></td>
					<td style='padding: 8px;'>- The <code>database.py</code> module establishes MongoDB connectivity for MediaMasterBot, exposing collections for users, groups, and statistics<br>- Provides helper functions to register new users and groups while preventing duplicates, and to retrieve user records<br>- Logs significant events such as bot initiation by a user or addition to a new group, enabling consistent data persistence across the bot’s operations.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/deviantart.py'>deviantart.py</a></b></td>
					<td style='padding: 8px;'>- The <code>deviantart.py</code> module downloads media from DeviantArt links, retrieves them through a proxy‑enabled extraction service, stores files locally, uploads them to Telegram chats, enforces channel subscription, throttles spam, tracks user activity, logs upload statistics, and cleans up temporary files, integrating with the bot’s anti‑spam, force‑subscribe, and database modules<br>- It validates user permissions, handles errors gracefully, records upload metrics, and removes temporary files after transfer, ensuring efficient resource usage within the bot’s modular architecture.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/download.py'>download.py</a></b></td>
					<td style='padding: 8px;'>- The <code>download.py</code> module creates and verifies a comprehensive Downloads folder hierarchy for diverse media sources, automatically generating any missing directories and logging the process<br>- This guarantees that subsequent download operations have a ready, organized storage structure across platforms such as Instagram, Pinterest, Reddit, and more, supporting the projects modular download functionality for users.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/errors.py'>errors.py</a></b></td>
					<td style='padding: 8px;'>- The <code>errors.py</code> module provides centralized error handling for the bot, capturing exceptions and logging them for debugging while notifying the user.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/force_sub.py'>force_sub.py</a></b></td>
					<td style='padding: 8px;'>- The <code>force_sub.py</code> module enforces channel membership before allowing media downloads, checking participant status, prompting users to join, and providing retry functionality via inline buttons<br>- It retrieves the target channel entity, constructs a message with a link button and a retry callback, and handles callback queries to confirm membership or alert the user<br>- This module integrates with the bot’s event loop to gate content access.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/group_add.py'>group_add.py</a></b></td>
					<td style='padding: 8px;'>- The <code>group_add.py</code> module adds a group to the database upon the bot’s first join, sends a welcome message explaining media download features, and temporarily flags the chat to avoid duplicate welcomes<br>- This module hooks into Telethon’s ChatAction events, coordinating with the database layer to track active groups and provide a smooth onboarding experience for users.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/hanime.py'>hanime.py</a></b></td>
					<td style='padding: 8px;'>- The <code>hanime.py</code> module manages HAnime video requests by validating user status, retrieving media data from locoloader, downloading video and thumbnail, uploading to Telegram, recording usage statistics, and enforcing anti‑spam and subscription rules while handling errors and cleaning temporary files<br>- It creates per‑user download</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/help.py'>help.py</a></b></td>
					<td style='padding: 8px;'>- The <code>help.py</code> module registers a /help command that, when triggered, sends a concise overview of all bot commands and their purposes, guiding users through available features such as song and video downloads, shazam identification, owner‑only utilities, and platform listings<br>- This module integrates with the Telethon event system, ensuring the help message is accessible from any chat where the bot is active.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/instagram.py'>instagram.py</a></b></td>
					<td style='padding: 8px;'>- The <code>instagram.py</code> module downloads Instagram media, uploads it to Telegram, manages user download state, enforces anti‑spam limits, logs progress, records upload statistics, and handles errors gracefully<br>- It integrates with the bot</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/listen.py'>listen.py</a></b></td>
					<td style='padding: 8px;'>- The <code>listen.py</code> module monitors incoming messages for media links across platforms such as YouTube, Twitter, Reddit, and adult sites, verifies user subscription status, and triggers corresponding download and upload routines to retrieve and forward media content<br>- By registering event handlers for each platform’s URL patterns, it centralizes link processing and enforces access controls before media handling.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/logs.py'>logs.py</a></b></td>
					<td style='padding: 8px;'>- The <code>logs.py</code> module provides a /logs command for the bot owner, reading recent entries from the Media‑Downloader.log, uploading them to SpaceB.in, and sending the log file back to the chat with a public link<br>- This module integrates logging utilities into the bot’s command framework, enabling quick diagnostics and remote log access for maintenance.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/nhentai.py'>nhentai.py</a></b></td>
					<td style='padding: 8px;'>- The <code>nhentai.py</code> module downloads nhentai content by extracting URLs through a proxy, converts images when necessary, uploads them to Telegram chats, and records usage statistics<br>- It enforces channel subscription, prevents spam, tracks user download status, and cleans up temporary files, integrating with the bot’s anti‑spam, database, and upload helper modules, ensuring smooth user experience across private and group chats.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/PerfectGirls.py'>PerfectGirls.py</a></b></td>
					<td style='padding: 8px;'>- Downloads PerfectGirls videos through a proxy‑enabled locoloader service, sanitizes filenames, streams media with yt_dlp, and uploads the result to Telegram chats while enforcing per‑user download limits and anti‑spam checks<br>- It records upload metrics, handles errors gracefully, and cleans temporary files, fitting into the bot’s modular architecture for media retrieval and distribution.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/pinterest.py'>pinterest.py</a></b></td>
					<td style='padding: 8px;'>- The <code>pinterest.py</code> module downloads Pinterest media, validates user access, and uploads content to chat, while enforcing anti‑spam rules, handling errors, logging activity, and recording usage statistics<br>- It orchestrates gallery‑dl calls, manages temporary storage, cleans up after uploads, and integrates with the bot’s user database and subscription checks,</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/pornhub.py'>pornhub.py</a></b></td>
					<td style='padding: 8px;'>- The <code>pornhub.py</code> module is for downloading videos from Pornhub, including anti-spam and user-tracking features.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/reddit.py'>reddit.py</a></b></td>
					<td style='padding: 8px;'>- The <code>reddit.py</code> module downloads Reddit media, converts streaming formats, and uploads the content to Telegram channels<br>- It verifies user subscription status, enforces anti‑spam limits, and records upload statistics<br>- The module interacts with a proxy API to fetch media URLs, handles image and video extraction, supports m3u8 conversion via yt‑dl, and cleans up temporary files after successful transfer.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/restart.py'>restart.py</a></b></td>
					<td style='padding: 8px;'>- The <code>restart.py</code> module enables the bot owner to trigger a graceful restart via the /restart command, records the chat and message identifiers to a JSON file for post‑restart updates, and re‑executes the Python interpreter to reload the bot<br>- This module integrates with the Telethon event system, ensuring controlled restarts within the overall bot architecture.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/rule34.py'>rule34.py</a></b></td>
					<td style='padding: 8px;'>- The <code>rule34.py</code> module handles user requests to fetch and deliver Rule34 media, integrating with Telethon event handling, enforcing</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/rule34video.py'>rule34video.py</a></b></td>
					<td style='padding: 8px;'>- The <code>rule34video.py</code> module downloads and uploads Rule34 videos on user request, enforcing anti‑spam limits, tracking user activity, and recording upload statistics<br>- It leverages yt_dlp for extraction, FastTelethonhelper for efficient uploads, and Telethon for messaging<br>- Errors are handled gracefully, temporary files are cleaned up after transfer, and progress is logged while updating last download timestamps to ensure only one download per user at a time.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/Shazam.py'>Shazam.py</a></b></td>
					<td style='padding: 8px;'>- The <code>Shazam.py</code> module handles user‑initiated song recognition by processing replied audio or video files, leveraging Shazam for identification, searching YouTube for the track, downloading the best audio, and uploading it back to the chat with metadata<br>- It integrates anti‑spam, force‑subscription enforcement, user state tracking, and upload statistics, ensuring smooth operation within the bot’s modular architecture.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/socigames.py'>socigames.py</a></b></td>
					<td style='padding: 8px;'>- The <code>socigames.py</code> module downloads Socigames video from a supplied URL, ensuring the requester is a subscribed member and not spamming<br>- It selects the highest‑resolution CDN link, streams the file to a temporary directory, uploads the media to the chat via Telethon, logs the upload size for analytics, and removes temporary files while updating user download status.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/song.py'>song.py</a></b></td>
					<td style='padding: 8px;'>- The <code>song.py</code> module validates the request, downloads the media from Spotify or YouTube, uploads it to a CDN, and logs the results, orchestrating the end-to-end flow from request to delivery.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/start.py'>start.py</a></b></td>
					<td style='padding: 8px;'>- The <code>start.py</code> module initiates user onboarding by registering a /start command that records new users, delivers a welcome message with media download instructions, and optionally sends a branded image<br>- It ensures smooth first interaction, logs user details, and provides a fallback text response if image delivery fails, integrating with the bot’s command handling and database modules.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/stats.py'>stats.py</a></b></td>
					<td style='padding: 8px;'>- The <code>stats.py</code> module provides owner‑only statistics interface, tracking upload counts and sizes across modules, computing uptime, and presenting paginated module details via inline buttons<br>- Records upload metrics in database, aggregates totals, and displays user count<br>- Integrates with Telethon event handlers to respond to /stats and callback queries, enabling real‑time monitoring of bot activity.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/supported_links.py'>supported_links.py</a></b></td>
					<td style='padding: 8px;'>- The <code>supported_links.py</code> module displays a list of all supported websites and services from which the bot can download media.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/System_Info.py'>System_Info.py</a></b></td>
					<td style='padding: 8px;'>- The <code>System_Info.py</code> module enables a /sysinfo command that gathers system information using neofetch, parses the output, formats it into a stylized</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/threads.py'>threads.py</a></b></td>
					<td style='padding: 8px;'>- The <code>threads.py</code> module downloads media from Threads links, verifies user eligibility, enforces anti‑spam limits, and streams each file to the chat via the bot<br>- It logs progress, records upload statistics, and cleans temporary files, ensuring smooth interaction across private and group contexts while maintaining database state and error resilience, and supports graceful recovery from network failures.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/tiktok.py'>tiktok.py</a></b></td>
					<td style='padding: 8px;'>- The <code>tiktok.py</code> module downloads TikTok media from user‑supplied links, streams the content through an external extraction service, and uploads the resulting files to the chat<br>- It enforces per‑user download limits and anti‑spam checks, logs progress, records upload statistics, and handles errors gracefully, ensuring an efficient and smooth user experience within the bot’s media‑handling architecture.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/twitter.py'>twitter.py</a></b></td>
					<td style='padding: 8px;'>- The <code>twitter.py</code> module downloads media from Twitter links, verifies that the requesting user is subscribed to the required channel, and applies anti‑spam limits to prevent abuse<br>- After successful download, the media is uploaded to the chat with a bot‑generated caption, while usage statistics are recorded<br>- Temporary files are removed</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/update.py'>update.py</a></b></td>
					<td style='padding: 8px;'>- The <code>update.py</code> module enables remote self‑update capabilities for the bot through a privileged command that pulls the latest repository changes, installs any new dependencies found in requirements.txt, and restarts the process to apply updates, ensuring continuous deployment within the overall architecture that integrates Telethon event handling with secure owner verification and automated reboot.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/xnxx.py'>xnxx.py</a></b></td>
					<td style='padding: 8px;'>- The <code>xnxx.py</code> module downloads Xnxx videos by extracting metadata through locoloader, streams the chosen 720p file, uploads</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/Xvideos.py'>Xvideos.py</a></b></td>
					<td style='padding: 8px;'>- The <code>Xvideos.py</code> module downloads Xvideos links by extracting metadata through a proxy‑enabled API, retrieves a 720p video stream, and uploads it to Telegram using FastTelethonhelper<br>- It enforces anti‑spam limits, tracks user download status, logs progress, records upload statistics, and cleans temporary files<br>- Errors are routed to a central handler, ensuring graceful recovery within the bot’s modular architecture.</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/youtube.py'>youtube.py</a></b></td>
					<td style='padding: 8px;'>- The <code>youtube.py</code> module downloads YouTube videos requested by users, verifies channel membership, throttles repeated requests, and streams the media to the chat<br>- It handles errors gracefully, informs users of subscription requirements</td>
				</tr>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='/Modules/youtubev2.py'>youtubev2.py</a></b></td>
					<td style='padding: 8px;'>- Orchestrates the end-to-end flow for YouTube downloads by handling Telethon events, enforcing anti-spam and subscription rules, and managing the entire download/upload pipeline.<br>- It connects the bot’s command interface with all necessary backend modules for media processing and user management.</td>
				</tr>
			</table>
		</blockquote>
	</details>
</details>

---

## Getting Started

### Prerequisites

This project requires the following dependencies:

- **Programming Language:** Python
- **Package Manager:** Pip

### Installation

Build  from the source and intsall dependencies:

1. **Clone the repository:**

    ```sh
    ❯ git clone https://github.com/SyntaxAdi/Media-Downloader-Bot
    ```

2. **Navigate to the project directory:**

    ```sh
    ❯ cd Media-Downloader-Bot
    ```

3. **Install the dependencies:**

   ```sh
   ❯ pip install -r requirements.txt
   ```

### Usage

Run the project with:

**Using python3:**
```sh
python3 akeno.py
```

**Using reloady for auto-reloading:**
```sh
reloady akeno.py
```

### Testing

This project is tested in a live production environment on Northflank and through self-based testing to ensure stability and performance.

---

## Roadmap

- [X] **`Core`**: Initial bot structure and core modules.
- [ ] **`Feature`**: Add support for more media websites.
- [ ] **`Improvement`**: Refactor and improve error handling.
- [ ] **`Documentation`**: Add detailed documentation for each module.

---

## Contributing

- **💬 [Join the Discussions](https://t.me/BotBuildersHQ)**: Share your insights, provide feedback, or ask questions.
- **🤖 [Use the Bot](https://t.me/AllLinksDLBot)**: Try out the bot and explore its features.
- **💡 [Suggest Features & Report Bugs](https://t.me/ItzAditya_xD)**: Share new ideas or let the owner know about any issues.

<details closed>
<summary>Contributing Guidelines</summary>

1. **Fork the Repository**: Start by forking the project repository to your LOCAL account.
2. **Clone Locally**: Clone the forked repository to your local machine using a git client.
   ```sh
   git clone https://github.com/SyntaxAdi/Media-Downloader-Bot
   ```
3. **Create a New Branch**: Always work on a new branch, giving it a descriptive name.
   ```sh
   git checkout -b new-feature-x
   ```
4. **Make Your Changes**: Develop and test your changes locally.
5. **Commit Your Changes**: Commit with a clear message describing your updates.
   ```sh
   git commit -m 'Implemented new feature x.'
   ```
6. **Push to LOCAL**: Push the changes to your forked repository.
   ```sh
   git push origin new-feature-x
   ```
7. **Submit a Pull Request**: Create a PR against the original project repository. Clearly describe the changes and their motivations.
8. **Review**: Once your PR is reviewed and approved, it will be merged into the main branch. Congratulations on your contribution!
</details>

<!--
<details closed>
<summary>Contributor Graph</summary>
<br>
<p align="left">
   <a href="https://LOCAL{///}graphs/contributors">
      <img src="https://contrib.rocks/image?repo=/">
   </a>
</p>
</details>
-->

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- Thanks to the creators of `readme-ai` for the template.

<div align="right">

[![][back-to-top]](#top)

</div>


[back-to-top]: https://img.shields.io/badge/-BACK_TO_TOP-151515?style=flat-square


---
