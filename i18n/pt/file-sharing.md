---
title: "Ferramentas de Autenticação Multi-Factor"
icon: material/share-variant
description: Descubra como partilhar os seus ficheiros em privado entre os seus dispositivos, com os seus amigos e família, ou anonimamente online.
---

Descubra como partilhar os seus ficheiros em privado entre os seus dispositivos, com os seus amigos e família, ou anonimamente online.

## Gestores de senhas

### OnionShare

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![logotipo OnionShare](/assets/img/file-sharing-sync/onionshare.svg){ align=right }
    
    **OnionShare** é uma ferramenta de código aberto que lhe permite partilhar de forma segura e anónima um ficheiro de qualquer tamanho. Funciona iniciando um servidor web acessível como um serviço Tor onion, com um URL indiscutível que você pode compartilhar com os destinatários para baixar ou enviar arquivos. [Visite onionshare.org](https://onionshare.org){ .md-button .md-button--primary } [:pg-tor:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .md-button }
    
    **Downloads***
    - [:fontawesome-brands-windows: Windows](https://onionshare.org/#download)
    - [:fontawesome-brands-apple: macOS](https://onionshare.org/#download)
    - [:fontawesome-brands-linux: Linux](https://onionshare.org/#download)
    - [:fontawesome-brands-github: Fonte](https://github.com/onionshare/onionshare) You can use other public instances, or you can host Send yourself.
    
    [:octicons-home-16: Homepage](https://send.vis.ee){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Public Instances"}
    [:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=Contribute }

Send can be used via its web interface or via the [ffsend](https://github.com/timvisee/ffsend) CLI. If you are familiar with the command-line and send files frequently, we recommend using the CLI client to avoid JavaScript-based encryption. You can specify the `--host` flag to use a specific server:

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### Buraco de Verme Mágico

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![logotipo FreedomBox](/assets/img/file-sharing-sync/freedombox.svg){ align=right }
    
    **FreedomBox** é um sistema operacional projetado para ser executado em um [computador de placa única (SBC)](https://en.wikipedia.org/wiki/Single-board_computer). O objetivo é facilitar a configuração de aplicações de servidor que você pode querer auto-hospedar.
    
    [Visite freedombox.org](https://freedombox.org){ .md-button .md-button--primary }
    
    **Downloads***
    - [:fontawesome-brands-git: Fonte](https://salsa.debian.org/freedombox-team/freedombox) downloads
    
        - [:simple-windows11: Windows](https://onionshare.org/#download)
        - [:simple-apple: macOS](https://onionshare.org/#download)
        - [:simple-linux: Linux](https://onionshare.org/#download)

### Framadate

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! Considere o auto-hospedagem para mitigar esta ameaça.

    ![logo PrivateBin](/assets/img/productivity/privatebin.svg){ align=right }
    
    **PrivateBin** é um pastebin online minimalista e de código aberto onde o servidor tem zero conhecimento de dados colados. Os dados são criptografados/descriptografados no navegador usando AES de 256 bits. Psono suporta compartilhamento seguro de senhas, arquivos, marcadores e e-mails.

- Must not store decrypted data on a remote server.
- Must be open-source software.
- Must either have clients for Linux, macOS, and Windows; or have a web interface.

## FreedomBox

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![FreedomBox logo](assets/img/file-sharing-sync/freedombox.svg){ align=right }
    
    **FreedomBox** is an operating system designed to be run on a [single-board computer (SBC)](https://en.wikipedia.org/wiki/Single-board_computer). The purpose is to make it easy to set up server applications that you might want to self-host.
    
    [:octicons-home-16: Homepage](https://freedombox.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title=Documentation}
    [:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://freedomboxfoundation.org/donate/){ .card-link title=Contribute }

## Sincronização de arquivos

### Nextcloud (Client-Server)

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![logotipo do LibreOffice](/assets/img/productivity/libreoffice.svg){ align=right }
    
    **LibreOffice** é uma suite de escritório gratuita e de código aberto com amplas funcionalidades.
    
    [Visite libreoffice.org](https://www.libreoffice.org){ .md-button .md-button--primary } [Política de Privacidade](https://www.libreoffice.org/about-us/privacy/privacy-policy-en/){ .md-button }
    
    **Downloads***
    - [:fontawesome-brands-windows: Windows](https://www.libreoffice.org/download/download/)
    - [:fontawesome-brands-apple: macOS](https://www.libreoffice.org/download/download/)
    - [:fontawesome-brands-linux: Linux](https://www.libreoffice.org/download/download/)
    - [:pg-flathub: Flatpak](https://www.libreoffice.org/download/download/)
    - [:fontawesome-brands-freebsd: FreeBSD](https://www.freshports.org/editors/libreoffice/)
    - [:pg-openbsd: OpenBSD](https://openports.se/editors/libreoffice)
    - [:pg-netbsd: NetBSD](https://pkgsrc.se/misc/libreoffice)
    - [:fontawesome-brands-google-play: Google Play](https://www.libreoffice.org/download/android-and-ios/)
    - [:fontawesome-brands-app-store-ios: App Store](https://www.libreoffice.org/download/android-and-ios/)
    - [:fontawesome-brands-git: Source](https://www.libreoffice.org/about-us/source-code) downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
        - [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
        - [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
        - [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
        - [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/www/nextcloud)

!!! Isto permite-nos fornecer recomendações completamente objectivas.</strong> Desenvolvemos um conjunto claro de requisitos para qualquer provedor de VPN que deseje ser recomendado, incluindo criptografia forte, auditorias de segurança independentes, tecnologia moderna, e muito mais.

    ![OnlyOffice logo](/assets/img/productivity/onlyoffice.svg){ align=right }
    
    **OnlyOffice** é uma alternativa, é uma suite de escritório gratuita e de código aberto com uma extensa funcionalidade.

### Syncthing (P2P)

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Syncthing logo](assets/img/file-sharing-sync/syncthing.svg){ align=right }
    
    **Syncthing** is an open-source peer-to-peer continuous file synchronization utility. It is used to synchronize files between two or more devices over the local network or the internet. Syncthing does not use a centralized server; it uses the [Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1) to transfer data between devices. All data is encrypted using TLS.
    
    [:octicons-home-16: Homepage](https://syncthing.net){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/syncthing){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://syncthing.net/donations/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nutomic.syncthingandroid)
        - [:simple-windows11: Windows](https://syncthing.net/downloads/)
        - [:simple-apple: macOS](https://syncthing.net/downloads/)
        - [:simple-linux: Linux](https://syncthing.net/downloads/)
        - [:simple-freebsd: FreeBSD](https://syncthing.net/downloads/)
        - [:simple-openbsd: OpenBSD](https://syncthing.net/downloads/)
        - [:simple-netbsd: NetBSD](https://syncthing.net/downloads/)

### Framadate

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! Considere o auto-hospedagem para mitigar esta ameaça.

    ![logo PrivateBin](/assets/img/productivity/privatebin.svg){ align=right }
    
    **PrivateBin** é um pastebin online minimalista e de código aberto onde o servidor tem zero conhecimento de dados colados. Os dados são criptografados/descriptografados no navegador usando AES de 256 bits. Psono suporta compartilhamento seguro de senhas, arquivos, marcadores e e-mails.

#### Minimum Requirements

- Must not require a third-party remote/cloud server.
- Must be open-source software.
- Must either have clients for Linux, macOS, and Windows; or have a web interface.

#### Best-Case

Our best-case criteria represents what we would like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Has mobile clients for iOS and Android, which at least support document previews.
- Supports photo backup from iOS and Android, and optionally supports file/folder sync on Android.
