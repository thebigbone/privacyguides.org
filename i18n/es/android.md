---
title: "Android"
icon: 'fontawesome/brands/android'
description: You can replace the operating system on your Android phone with these secure and privacy-respecting alternatives.
---

![Android logo](assets/img/android/android.svg){ align=right }

El **proyecto de código abierto de Android** es un sistema operativo móvil de código abierto liderado por Google, que está detrás de la mayor parte de los dispositivos móviles del mundo. La mayor parte de los teléfono vendidos con Android son modificados para incluir integraciones y aplicaciones invasivas como los servicios de Google Play, así que puedes mejorar la privacidad de tu dispositivo móvil de manera significativa al reemplazar la instalación predeterminada de tu teléfono con una versión de Android sin esas características invasivas.

[:octicons-home-16:](https://source.android.com/){ .card-link title=Inicio }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentación}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/){ .card-link title="Código fuente" }

En particular, GrapheneOS admite [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play). Los Servicios de Google Play se pueden ejecutar completamente de manera aislada como una aplicación de usuario normal y se pueden incluir en un [perfil de trabajo o un perfil de usuario](#android-security-privacy) de su elección.

[General Android Overview :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

[Why we recommend GrapheneOS over CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/ ""){.md-button}

## Derivados de AOSP

We recommend installing one of these custom Android operating systems on your device, listed in order of preference, depending on your device's compatibility with these operating systems.

!!! note

    ![Logotipo de GrapheneOS](assets/img/android/grapheneos.svg#only-light){ align=right }
    ![Logotipo de GrapheneOS ](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }
    
    **GrapheneOS** es la mejor opción cuando se trata de privacidad y seguridad. GrapheneOS proporciona mejoras adicionales de [seguridad](https://es.wikipedia.org/wiki/Endurecimiento_(inform%C3%A1tica)) y de privacidad.

### GrapheneOS

!!! recomendación

    Los dispositivos de "soporte extendido" de GrapheneOS no tienen correcciones de seguridad completos (actualizaciones de firmware) debido a que el fabricante de equipos originales (OEM) suspende el soporte.
    
    Estos dispositivos no pueden considerarse completamente seguros. Dispone de un [asignador de memoria reforzado](https://github.com/GrapheneOS/hardened_malloc), permisos de red y de sensores, y otras [características de seguridad](https://grapheneos.org/features). GrapheneOS también incluye actualizaciones completas de firmware y compilaciones firmadas, por lo que el arranque verificado es totalmente compatible.
    
    [:octicons-home-16: Inicio](https://grapheneos.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Política de privacidad" }
    [:octicons-info-16:](https://grapheneos.org/faq/){ .card-link title=Documentación}
    [:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Código fuente" }
    [:octicons-heart-16:](https://grapheneos.org/donate/){ .card-link title=Contribuir }

GrapheneOS supports [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), which runs [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) fully sandboxed like any other regular app. This means you can take advantage of most Google Play Services, such as [push notifications](https://firebase.google.com/docs/cloud-messaging/), while giving you full control over their permissions and access, and while containing them to a specific [work profile](os/android-overview.md#work-profile) or [user profile](os/android-overview.md#user-profiles) of your choice.

Google Pixel phones are the only devices that currently meet GrapheneOS's [hardware security requirements](https://grapheneos.org/faq#device-support).

### CalyxOS

!!! recomendación

    ![CalyxOS logo](assets/img/android/calyxos.svg){ align=right }
    
    **CalyxOS** es una alternativa aceptable a GrapheneOS.
    Tiene algunas funciones de privacidad además de AOSP, que incluyen [Datura firewall](https://calyxos.org/docs/tech/datura-details), [Signal](https://signal.org) integración en la aplicación de marcación y un botón de pánico incorporado. CalyxOS también viene con actualizaciones de firmware y compilaciones firmadas, así que [el arranque verificado](https://source.android.com/security/verifiedboot) es completamente compatible.
    
    [:octicons-home-16: Inicio](https://divestos.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Servicio Onion" }
    [:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Politica de privacidad" }
    [:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Documentación}
    [:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Código fuente" }
    [:octicons-heart-16:](https://divested.dev/index.php?page=donate){ .card-link title=Contribuir }

DivestOS has automated kernel vulnerability ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [patching](https://gitlab.com/divested-mobile/cve_checker), fewer proprietary blobs, and a custom [hosts](https://divested.dev/index.php?page=dnsbl) file. Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates. DivestOS also includes kernel patches from GrapheneOS and enables all available kernel security features via [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). All kernels newer than version 3.4 include full page [sanitization](https://lwn.net/Articles/334747/) and all ~22 Clang-compiled kernels have [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) enabled.

DivestOS implements some system hardening patches originally developed for GrapheneOS. DivestOS 16.0 and higher implements GrapheneOS's [`INTERNET`](https://developer.android.com/training/basics/network-ops/connecting) and SENSORS permission toggle, [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constification](https://en.wikipedia.org/wiki/Const_(computer_programming)), and partial [bionic](https://en.wikipedia.org/wiki/Bionic_(software)) hardening patchsets. 17.1 and higher features GrapheneOS's per-network full [MAC randomization](https://en.wikipedia.org/wiki/MAC_address#Randomization) option, [`ptrace_scope`](https://www.kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, and automatic reboot/Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features).

DivestOS uses F-Droid as its default app store. Normally, we would recommend avoiding F-Droid due to its numerous [security issues](#f-droid). However, doing so on DivestOS isn't viable; the developers update their apps via their own F-Droid repositories ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) and [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). We recommend disabling the official F-Droid app and using [Neo Store](https://github.com/NeoApplications/Neo-Store/) with the DivestOS repositories enabled to keep those components up to date. For other apps, our recommended methods of obtaining them still apply.

!!! warning

    La actualización del firmware de DivestOS [status](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) y el control de calidad varían según los dispositivos que soporta. Seguimos recomendando GrapheneOS en función de la compatibilidad de tu dispositivo. Para otros dispositivos, DivestOS es una buena alternativa.
    
    No todos los dispositivos compatibles tienen arranque verificado y algunos lo realizan mejor que otros.

## Dispositivos Android

When purchasing a device, we recommend getting one as new as possible. The software and firmware of mobile devices are only supported for a limited time, so buying new extends that lifespan as much as possible.

Avoid buying phones from mobile network operators. These often have a **locked bootloader** and do not support [OEM unlocking](https://source.android.com/devices/bootloader/locking_unlocking). These phone variants will prevent you from installing any kind of alternative Android distribution.

Be very **careful** about buying second hand phones from online marketplaces. Always check the reputation of the seller. If the device is stolen, there's a possibility of [IMEI blacklisting](https://www.gsma.com/security/resources/imei-blacklisting/). There is also a risk involved with you being associated with the activity of the previous owner.

A few more tips regarding Android devices and operating system compatibility:

- Do not buy devices that have reached or are near their end-of-life, additional firmware updates must be provided by the manufacturer.
- Do not buy preloaded LineageOS or /e/ OS phones or any Android phones without proper [Verified Boot](https://source.android.com/security/verifiedboot) support and firmware updates. These devices also have no way for you to check whether they've been tampered with.
- In short, if a device or Android distribution is not listed here, there is probably a good reason. Check out our [forum](https://discuss.privacyguides.net/) to find details!

### DivestOS

Google Pixel phones are the **only** devices we recommend for purchase. Pixel phones have stronger hardware security than any other Android devices currently on the market, due to proper AVB support for third-party operating systems and Google's custom [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) security chips acting as the Secure Element.

!!! recomendación

    ![Logotipo de DivestOS](assets/img/android/divestos.svg){ align=right }
    
    **DivestOS** es un [soft-fork](https://es. wikipedia.org/wiki/Bifurcaci%C3%B3n_(desarrollo_de_software)) de [LineageOS](https://lineageos.org/).
    
    DivestOS hereda muchos [dispositivos soportados](https://divestos.org/index.php?page=devices&base=LineageOS) de LineageOS.
    
    Tiene builds firmados, lo que permite tener [arranque verificado](https://source.android.com/security/verifiedboot) en algunos dispositivos que no son Pixel.

Secure Elements like the Titan M2 are more limited than the processor's Trusted Execution Environment used by most other phones as they are only used for secrets storage, hardware attestation, and rate limiting, not for running "trusted" programs. Phones without a Secure Element have to use the TEE for *all* of those functions, resulting in a larger attack surface.

Google Pixel phones use a TEE OS called Trusty which is [open-source](https://source.android.com/security/trusty#whyTrusty), unlike many other phones.

The installation of GrapheneOS on a Pixel phone is easy with their [web installer](https://grapheneos.org/install/web). If you don't feel comfortable doing it yourself and are willing to spend a bit of extra money, check out the [NitroPhone](https://shop.nitrokey.com/shop) as they come preloaded with GrapheneOS from the reputable [Nitrokey](https://www.nitrokey.com/about) company.

A few more tips for purchasing a Google Pixel:

- If you're after a bargain on a Pixel device, we suggest buying an "**a**" model, just after the next flagship is released. Discounts are usually available because Google will be trying to clear their stock.
- Consider price beating options and specials offered at physical stores.
- Look at online community bargain sites in your country. These can alert you to good sales.
- Google provides a list showing the [support cycle](https://support.google.com/nexus/answer/4457705) for each one of their devices. The price per day for a device can be calculated as: $\text{Cost} \over \text {EOL Date}-\text{Current Date}$, meaning that the longer use of the device the lower cost per day.

## Aplicaciones generales

We recommend a wide variety of Android apps throughout this site. The apps listed here are Android-exclusive and specifically enhance or replace key system functionality.

### Perfiles de usuario

!!! recomendación

    ![Logotipo de Shelter](assets/img/android/shelter.svg){ align=right }
    
    **Shelter** es una aplicación que te ayuda a aprovechar la funcionalidad perfil de trabajo de Android para aislar o duplicar aplicaciones en tu dispositivo.
    
    Shelter permite bloquear la búsqueda de contactos entre perfiles y compartir archivos entre perfiles a través del gestor de archivos predeterminado ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).
    
    [:octicons-repo-16: Repositorio](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Código fuente" }
    [:octicons-heart-16:](https://www.patreon.com/PeterCxy){ .card-link title=Contribuir }
    
    ??? descargas
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.typeblog.shelter)

!!! warning

    Se recomienda Shelter en lugar de [Insular](https://secure-system.gitlab.io/Insular/) e [Island](https://github.com/oasisfeng/island), ya que admite [bloqueo de búsqueda de contactos](https://secure-system.gitlab.io/Insular/faq.html).
    
    Al usar Shelter, está depositando toda su confianza en su desarrollador, ya que Shelter actúa como [Administrador de dispositivos](https://developer.android.com/guide/topics/admin/device-admin) para crear el perfil de trabajo, y tiene un amplio acceso a los datos almacenados en él.

### Perfil de trabajo

!!! recomendación

    ![Logo Auditor](assets/img/android/auditor.svg#only-light){ align=right }
    ![Logo Auditor ](assets/img/android/auditor-dark.svg#only-dark){ align=right }
    
    **Auditor** es una aplicación que aprovecha las funciones de seguridad del hardware para supervisar la integridad de los dispositivos [compatibles](https://attestation.app/about#device-support). Actualmente, sólo funciona con GrapheneOS y con el sistema operativo original del dispositivo.
    
    [:octicons-home-16: Inicio](https://attestation.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Politica de privacidad" }
    [:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentación}
    [:octicons-code-16:](https://attestation.app/source){ .card-link title="Código fuente" }
    [:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

Auditor performs attestation and intrusion detection by:

- Using a [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) model between an *auditor* and *auditee*, the pair establish a private key in the [hardware-backed keystore](https://source.android.com/security/keystore/) of the *Auditor*.
- The *auditor* can either be another instance of the Auditor app or the [Remote Attestation Service](https://attestation.app).
- The *auditor* records the current state and configuration of the *auditee*.
- Should tampering with the operating system of the *auditee* happen after the pairing is complete, the auditor will be aware of the change in the device state and configurations.
- You will be alerted to the change.

No personally identifiable information is submitted to the attestation service. We recommend that you sign up with an anonymous account and enable remote attestation for continuous monitoring.

If your [threat model](basics/threat-modeling.md) requires privacy, you could consider using [Orbot](tor.md#orbot) or a VPN to hide your IP address from the attestation service. To make sure that your hardware and operating system is genuine, [perform local attestation](https://grapheneos.org/install/web#verifying-installation) immediately after the device has been installed and prior to any internet connection.

### Arranque verificado

!!! recomendación

    ![Logo de Secure Camera](assets/img/android/secure_camera.svg#only-light){ align=right }
    ![Logo de Secure camera](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }
    
    **Secure Camera** es una aplicación de cámara centrada en la privacidad y la seguridad que puede capturar imágenes, vídeos y códigos QR. Las extensiones de proveedor de CameraX (Retrato, HDR, Visión nocturna, Retoque facial y Auto) también son compatibles con los dispositivos disponibles.
    
    [:octicons-repo-16: Repositorio](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
    [:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentación}
    [:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Código fuente" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuir }
    
    ??? descargas
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

Main privacy features include:

- Auto removal of [Exif](https://en.wikipedia.org/wiki/Exif) metadata (enabled by default)
- Use of the new [Media](https://developer.android.com/training/data-storage/shared/media) API, therefore [storage permissions](https://developer.android.com/training/data-storage) are not required
- Microphone permission not required unless you want to record sound

!!! note

    Actualmente no se eliminan los metadatos de los archivos de vídeo, pero está previsto hacerlo.
    
    Los metadatos de orientación de la imagen no se borran. Si habilitas la ubicación (en la cámara segura), * * tampoco se eliminará * *. Si quieres borrarlo más tarde tendrás que utilizar una aplicación externa como [ExifEraser](data-redaction.md#exiferaser).

### Visor seguro de PDF

!!! recomendación

    ![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
    ![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }
    
    **Secure PDF Viewer** es un visor de PDF basado en [pdf.js](https://en.wikipedia.org/wiki/PDF.js) que no requiere permisos. El PDF se introduce en un [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(desarrollo_software)) [webview](https://developer.android.com/guide/webapps/webview). Esto significa que no necesita permiso para acceder directamente a contenidos o archivos.
    
    [Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) se utiliza para garantizar que las propiedades de JavaScript y de estilo dentro de WebView sean enteramente de contenido estático.
    
    [:octicons-repo-16: Repositorio](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Código fuente" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuir }
    
    ??? descargas
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

## Obteniendo Aplicaciones

### Tienda de aplicaciones GrapheneOS

GrapheneOS's app store is available on [GitHub](https://github.com/GrapheneOS/Apps/releases). It supports Android 12 and above and is capable of updating itself. The app store has standalone applications built by the GrapheneOS project such as the [Auditor](https://attestation.app/), [Camera](https://github.com/GrapheneOS/Camera), and [PDF Viewer](https://github.com/GrapheneOS/PdfViewer). If you are looking for these applications, we highly recommend that you get them from GrapheneOS's app store instead of the Play Store, as the apps on their store are signed by the GrapheneOS's project own signature that Google does not have access to.

### Orbot

The Google Play Store requires a Google account to login which is not great for privacy. You can get around this by using an alternative client, such as Aurora Store.

!!! recomendación

    ![Logo Aurora Store](assets/img/android/aurora-store. ebp){ align=right }
    
    **Aurora Store** es un cliente de Google Play Store que no requiere de una cuenta de Google, Servicios Google Play, o microG para descargar aplicaciones.
    
    [:octicons-home-16: Página del proyecto](https://auroraoss.com/){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Código fuente" }
    
    ??? Descarga
    
        - [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

Aurora Store does not allow you to download paid apps with their anonymous account feature. You can optionally log in with your Google account with Aurora Store to download apps you have purchased, which does give access to the list of apps you've installed to Google, however you still benefit from not requiring the full Google Play client and Google Play Services or microG on your device.

### Shelter

For apps that are released on platforms like GitHub and GitLab, you may be able to add an RSS feed to your [news aggregator](/news-aggregators) that will help you keep track of new releases.

![RSS APK](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](./assets/img/android/rss-changes-light.png#only-light) ![APK Changes](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

On GitHub, using [Secure Camera](#secure-camera) as an example, you would navigate to its [releases page](https://github.com/GrapheneOS/Camera/releases) and append `.atom` to the URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

On GitLab, using [Aurora Store](#aurora-store) as an example, you would navigate to its [project repository](https://gitlab.com/AuroraOSS/AuroraStore) and append `/-/tags?format=atom` to the URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### Comprobando Firmas de las APK

If you download APK files to install manually, you can verify their signature with the [`apksigner`](https://developer.android.com/studio/command-line/apksigner) tool, which is a part of Android [build-tools](https://developer.android.com/studio/releases/build-tools).

1. Instala [Java JDK](https://www.oracle.com/java/technologies/downloads/).

2. Descarga las [herramientas de línea de comandos de Android Studio](https://developer.android.com/studio#command-tools).

3. Extrae el archivo descargado:

    ```bash
    unzip commandlinetools-*.zip
    cd cmdline-tools
    ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
    ```

4. Ejecuta el comando de verificación de firmas:

    ```bash
    ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
    ```

5. Los hashes resultantes pueden compararse con otra fuente. Algunos desarrolladores como Signal [muestran las firmas](https://signal.org/android/apk/) en su sitio web.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### Auditor

![F-Droid logo](assets/img/android/f-droid.svg){ align=right width=120px }

==We do **not** currently recommend F-Droid as a way to obtain apps.== F-Droid is often recommended as an alternative to Google Play, particularly in the privacy community. The option to add third-party repositories and not be confined to Google's walled garden has led to its popularity. F-Droid additionally has [reproducible builds](https://f-droid.org/en/docs/Reproducible_Builds/) for some applications and is dedicated to free and open-source software. However, there are [notable problems](https://privsec.dev/posts/android/f-droid-security-issues/) with the official F-Droid client, their quality control, and how they build, sign, and deliver packages.

Due to their process of building apps, apps in the official F-Droid repository often fall behind on updates. F-Droid maintainers also reuse package IDs while signing apps with their own keys, which is not ideal as it gives the F-Droid team ultimate trust.

Other popular third-party repositories such as [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) alleviate some of these concerns. The IzzyOnDroid repository pulls builds directly from GitHub and is the next best thing to the developers' own repositories. However, it is not something that we can recommend, as apps are typically [removed](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) from that respository when they make it to the main F-Droid repository. While that makes sense (since the goal of that particular repository is to host apps before they're accepted into the main F-Droid repository), it can leave you with installed apps which no longer receive updates.

That said, the [F-Droid](https://f-droid.org/en/packages/) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) repositories are home to countless apps, so they can be a useful tool to search for and discover open-source apps that you can then download through Play Store, Aurora Store, or by getting the APK directly from the developer. It is important to keep in mind that some apps in these repositories have not been updated in years and may rely on unsupported libraries, among other things, posing a potential security risk. You should use your best judgement when looking for new apps via this method.

!!! note

    En algunos raros casos, el desarrollador de una aplicación sólo la distribuirá a través de F-Droid ([Gadgetbridge](https://gadgetbridge.org/) es un ejemplo de ello). Si realmente necesitas una aplicación como esa, te recomendamos que utilices [Neo Store](https://github.com/NeoApplications/Neo-Store/) en lugar de la aplicación oficial F-Droid para obtenerla.

## Criterios

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! example "This section is new"

    Estamos trabajando para establecer criterios definidos para cada sección de nuestro sitio, y esto puede estar sujeto a cambios. Si tienes alguna duda sobre nuestros criterios, por favor [pregunta en nuestro foro](https://discuss.privacyguides.net/latest) y no asumas que no hemos tenido en cuenta algo a la hora de hacer nuestras recomendaciones si no aparece aquí. Son muchos los factores que se tienen en cuenta y se debaten cuando recomendamos un proyecto, y documentar cada uno de ellos es un trabajo en curso.

### Sistema Operativo

- Must be open-source software.
- Must support bootloader locking with custom AVB key support.
- Must receive major Android updates within 0-1 months of release.
- Must receive Android feature updates (minor version) within 0-14 days of release.
- Must receive regular security patches within 0-5 days of release.
- Must **not** be "rooted" out of the box.
- Must **not** enable Google Play Services by default.
- Must **not** require system modification to support Google Play Services.

### Dispositivo

- Must support at least one of our recommended custom operating systems.
- Must be currently sold new in stores.
- Must receive a minimum of 5 years of security updates.
- Must have dedicated secure element hardware.

### Aplicaciones

- Applications on this page must not be applicable to any other software category on the site.
- General applications should extend or replace core system functionality.
- Applications should receive regular updates and maintenance.
