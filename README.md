# BTG-Media-Hub
This desktop application was developed by me from January to April 2024 during my internship at BTG Pactual.

## Description and motivation
BTG Media Hub allows all BTG collaborators to watch and listen to channels available on office TVs directly from their laptops. Many users expressed a desire to hear broadcasts, not just watch them. This app resolves that issue, making it simple for everyone to access their preferred content from their own laptops.

![image](https://github.com/Henrique-Assme/BTG-Media-Hub/assets/69920692/10c91383-697d-48be-9078-4c99b8089397)

## How It Works
Using the application is straightforward — simply click on the image of the desired channel, and the respective broadcast will open using the MPV player. The images refresh periodically to reflect the current stream. The sidebar contains two buttons: "Home" refreshes all images to the latest available, and "Controls" displays shortcuts for controlling the broadcast via MPV.

![image](https://github.com/Henrique-Assme/BTG-Media-Hub/assets/69920692/22180f80-31ed-4fc3-a62d-a93db78c42fb)

##  Technology Stack
The entire application was built using Python. The front-end was developed with tkinter and custom tkinter libraries to create a modern UI, including the sidebar gradient and scrollable buttons area. Additionally, a server was implemented in Python to provide screenshots periodically to clients (using ffmpeg), manage connection URLs, and handle transcoding.

Transcoding is essential because the server adjusts URLs based on the client's connection type (wired or wireless). Clients connected via wired networks receive UDP URLs, while clients on WiFi request transcoded TCP URLs for stable streaming. This approach optimizes streaming capabilities and server load management.

The client also integrates with Microsoft's Active Directory for access control, ensuring only authorized users can use the application. This control helps monitor server load and user activity.

Another crucial aspect of the project is customizing MPV shortcuts by editing the input.conf file. Default shortcuts are disabled, allowing only essential shortcuts to function.

## Final Thoughts
This project was a significant challenge over four months. I worked independently, with occasional support from my team when needed. Developing in Python was initially unfamiliar but proved rewarding. I successfully implemented this application based on a superior's idea, enhancing my skills as a software engineer, problem solver, and self-starter.

Here's an image of the application with an MPV instance open:

![image](https://github.com/Henrique-Assme/BTG-Media-Hub/assets/69920692/f44e664f-0000-473f-a7c6-fd8709404827)
