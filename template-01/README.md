<p align="center">
  <a href="https://github.com/MuhammadAshouri/marzban-templates" target="_blank" rel="noopener noreferrer" >
    <img src="https://github.com/MuhammadAshouri/marzban-templates/blob/dca23a0ecbee84839686a1b928a2dc7e8aba4089/template-01/screenshot.jpg" alt="SubPage screenshots" width="800" height="auto">
  </a>
</p>

# Usage

First you need to copy [html file](https://github.com/MuhammadAshouri/marzban-templates/blob/master/template-01/index.html) to your sever. You can do it by this:

```bash
cd /opt/marzban
apt install wget
wget https://cdn.jsdelivr.net/gh/lunoxxdev/marhabantemplet@main/template-01/index.html
```

Then you have to map it to your docker container. Add this line to volume section of `docker-compose.yml`:

(DO NOT REPLACE WHOLE FILE, Just the last line)
```docker
services:
    marzban:
        ...
        volumes:
            ...
            - /opt/marzban/index.html:/code/app/templates/subscription/index.html # this line
```

Now you can restart your marzban's docker:
```
marzban restart
```

# Edit

You can change default settings from settings variable in index.html, [here](https://github.com/MuhammadAshouri/marzban-templates/blob/120817c45e2af843a3724ba9fe2018519ddc63b4/template-01/index.html#L194C19-L194C19) line 194

You can also change tutorial from appsJson variable in index.html, [here](https://github.com/MuhammadAshouri/marzban-templates/blob/3328559ea73e5a884fa0a619332ab1a040221395/template-01/index.html#L112C14-L112C14) line 25

For tutorial video, you need to set direct link of video to tutorial of json

To change logo you can change src in line 226
