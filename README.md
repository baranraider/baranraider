### 👋 Hello, I'm ra1der. I am interested in the FiveM platform and I am still in the learning phase.



## Socials
[![Discord](https://img.shields.io/badge/Discord-%237289DA.svg?logo=discord&logoColor=white)](https://discord.gg/wilddevelopment) 
[![Twitch](https://img.shields.io/badge/Twitch-%239146FF.svg?logo=Twitch&logoColor=white)](https://twitch.tv/ra1derlive) 
[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?logo=YouTube&logoColor=white)](https://www.youtube.com/channel/UCgSXZ-Vmasr5-tgzjpAmSyA) 

# Languages and Tools:
![Lua](https://img.shields.io/badge/lua-%232C2D72.svg?style=for-the-badge&logo=lua&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
<p align="left"> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> </p>

const axios = require("axios")

// Retrieve existing counter and increment for this view
// See https://docs.pipedream.com/workflows/steps/code/state/
const counter = $checkpoint + 1 || 1

// Use shields.io to generate a badge with our counter as the message
const { data } = await axios({
  url: `https://img.shields.io/static/v1?label=Profile-Views&message=${counter}&color=green`,
})

// Save the incremented counter back to state
$checkpoint = counter

// See https://docs.pipedream.com/workflows/steps/triggers/#customizing-the-http-response
$respond({
  status: 200,
  headers: {
    'Content-Type': 'image/svg+xml',
    'Cache-Control': 'max-age=0, no-cache, no-store, must-revalidate'
  },
  body: data,
}) 

