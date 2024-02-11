---
title: "Discord as a cloud storage"
description: "Using Discord to store files greater than 25MB without discord nitro"
dateString: Feb 2023 - current
draft: false
tags: ["NodeJS", "MongoDB", "Express", "Python", "File Chunking", "Threads"]
showToc: false
weight: 201
cover:
    image: "/projects/discord/discord.webp"
--- 
### 🔗 [GitHub](https://github.com/ManemDhanush/discord-storage-system)

## Description
I developed a cloud-based storage system using Discord that allows users to upload and share large files seamlessly. The project utilizes **Python**, **Node.js**, **MongoDB**, and **file chunking** to provide robust functionality. I designed a Discord bot with **JavaScript** and the **Discord.JS** library that interacts with users and handles file uploads. A key component is the chunking algorithm I created, which splits files into *25MB* parts for optimized storage and transmission.

The backend was built with Node.js and provides REST APIs for uploading and downloading files. MongoDB offers structured storage for metadata like file names, sizes, and the channel ID and thread ID for each 25MB chunk. The backend reconstructs the original file from the chunks stored in Discord channels and threads when a user downloads a file. This avoids the need for a separate CDN.

![Attention Mechanism](/projects/discord/filechunking.png)

To complete the project, I developed an intuitive React-based frontend that calls the Node.js APIs. It retrieves the channel ID and thread ID for each chunk and pieces the chunks back together into the original file for a seamless user experience. The frontend also displays file information like name, size, and upload progress. This cloud-based Discord file storage bot makes sharing large files easy for server members.