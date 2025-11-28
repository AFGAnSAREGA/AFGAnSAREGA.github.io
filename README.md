# AFGAnSAREGA.github.io

## JitPack Repository Configuration

To use JitPack in your Maven project, add the following repository configuration to your `pom.xml`:

```xml
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>
```

## Lidarr on Steroids Docker Setup

To run Lidarr on Steroids with Docker, use the following command:

```bash
docker run \
  --name lidarr \
  -p 8686:8686 \
  -p 6595:6595 \
  -v <path>:/config \
  -v <path>:/config_deemix \
  -v <path>:/downloads \
  -v <path>:/music \
  --restart unless-stopped \
  youegraillot/lidarr-on-steroids
```

Replace `<path>` with your actual directory paths for:
- `/config` - Lidarr configuration directory
- `/config_deemix` - Deemix configuration directory
- `/downloads` - Downloads directory
- `/music` - Music library directory