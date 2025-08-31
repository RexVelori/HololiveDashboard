# 🎬 VTuber Stream Dashboard

The **VTuber Stream Dashboard** is a lightweight web app to track the latest uploads from your favorite VTubers.  
It comes preloaded with Hololive EN generations and also supports adding indie channels directly in the config.

🔗 **Live Demo:** <https://rexvelori.github.io/HololiveDashboard/>

------------------------------------------------------------------------

## ✨ Features

-   Preloaded Hololive EN generations (Myth, Promise, Advent, Justice, Indie)
-   Toggle visibility of channels dynamically (per member or per generation)
-   Displays recent videos per channel (pulled from YouTube’s RSS feeds)
-   Shorts (`/shorts/…`) are automatically ignored
-   Video thumbnails, titles, and publish dates
-   Responsive, modern design with gradient background
-   No dependencies — built with **vanilla HTML, CSS, and JavaScript**

------------------------------------------------------------------------

## 🚀 How to Use

1.  Open the `index.html` file in any modern browser, or visit the live demo link above.  
2.  Click on a Hololive EN generation or individual member to activate them.  
3.  The latest videos for that member/channel will appear in the dashboard.  
4.  Toggle members or generations again to hide them.  
5.  Click on a video thumbnail to watch it directly on YouTube.

------------------------------------------------------------------------

## ⚙️ Configuration

Channels are defined in the `CONFIG` object near the top of `index.html`.  
To add your own indie channels, simply add them under a `group` in the config:

```js
{
  key: 'indie',
  label: 'Indie',
  members: [
    { id: 'UCxxxxxx', name: 'MyIndieVTuber' }
  ]
}
```

You can also set `defaultActive: true` if you want all channels to load automatically on page load.

------------------------------------------------------------------------

## 🛠️ Development

-   Built with **HTML, CSS, and JavaScript (vanilla)**  
-   Fetches video data via YouTube's public **RSS feeds**  
-   Uses **CORS proxy** to bypass fetch restrictions  

Note: YouTube’s RSS feeds only return the most recent ~15 videos per channel.

------------------------------------------------------------------------

## 📜 License

This project is open source. Feel free to fork and modify it for your
own use.
