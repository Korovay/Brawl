# BRAWL STARS
[ua.csv](https://github.com/Korovay/MULTiFRUiT/blob/main/ua.csv) - Here is the fully translated ```localization/ua.csv``` file in Ukrainian.

```// In the section where profileIconUrl is defined
let profileIconUrl;

// Check if a GIF version of the icon exists
const gifIconUrl = `https://korovay.github.io/MULTiFRUiT/Gif-Profile-Icons/${player.icon?.id}.gif`;
const pngIconUrl = `https://cdn.brawlify.com/profile-icons/regular/${player.icon?.id}.png`;

// Use axios to check the availability of the GIF file
try {
    const response = await axios.head(gifIconUrl);
    if (response.status === 200) {
        // If the GIF exists, use it
        profileIconUrl = gifIconUrl;
    } else {
        // If the GIF is not found, use the PNG
        profileIconUrl = pngIconUrl;
    }
} catch (error) {
    // In case of any error (e.g., 404), use the PNG
    profileIconUrl = pngIconUrl;
}```

