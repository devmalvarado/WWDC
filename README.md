Version en castellano (español) para latinoamérica e hispanohablantes

# WWDC app No Oficial para macOS 

Disfruta la Conferencia de Desarrolladores de Apple (Apple Worldwide Developers Conference) desde el comfort de tu Mac con la aplicación No Oficial de la WWDC para macOS. Asistas (virtualmente) o no, puedes acceder a las transmisiones en vivo, videos y sesiones durante la conferencia como un recurso durante todo el año.

En asociación con CocoaHub, también puedes usar la pestaña Community de la app para navegar a través de los anuncios de Apple, actualizaciones del lenguaje Swift, nuevos episodios de tus podcast favoritos, posts de los blogs de la comunidad y más.

⬇️ Si solo quieres descargar el ultimo lanzamiento,  visita [el sitio](https://wwdc.io).

## Horario (Schedule)

La pestaña de horario (schedule) muestra el horario de la edición actual de la WWDC, y te permite ver las transmisiones en vivo  de la  Keynote (conferencia principal) y de otras sesiones de la semana.

## Videos

Mira los videos de este año conforme sean lanzados y accede a los videos de los años anteriores. Puedes tambien leer las transcripciones de las sesiones y facilmente brincar a un punto específico en el video relevante. Las transcripciones también son buscables  y disponibles en ![videos](./screenshots/v7/Transcript.png)

### Características de Video 

- Mira los videos en velocidad 0.5x, 1x, 1.25x, 1.5x, 1.75x o 2x
- Pantalla completa y soporte nativo imagen en imagen (Picture in Picture)
- Navega en contenido de video facilmente con la ayuda de las transcripciones.

### Compartir Clips (Clip Sharing)

Compartir clips (Clip Sharing) te permite compartir un segmento corto (hasta 5 minutos) de un video de sesión. Esta es una gran característica para compartir rápidamente segmentos de contenido de la conferencia. 

![clipsharing](./screenshots/v7/ClipSharing.png)

## Chromecast

Puedes mirar Videos (ambos en vivo y bajo demanda) en tu Chromecast. Solo dale click al botón Chromecast mientras reproduces el video, escoge tu dispositivo de la lista y controlalo usando la aplicación Google Home en tu teléfono

![chromecast](./screenshots/v7/ChromeCast.png)

## Marcadores

¿Alguna vez te has encontrado mirando una sesion de la WWDC y deseando poder tomar notas en un punto específico en el video para referencia después? Esto es ahora posible con los marcadores.

Con los marcadores, puedes crear un punto de referencia dentro de un video y agregar una anotación en él. Tus anotaciones de marcadores también serán consideradas cuando hagas una búsqueda, por lo que es más fácil que unca encontrar contenido que marcaste antes.

![bookmarks](./screenshots/v7/Video-Bookmark.png)

## Comunidad

Explore el contenido seleccionado por el equipo [CocoaHub](http://cocoahub.app) en la pestaña Comunidad.

![community](./screenshots/v7/Community.png)

## Sincronización iCloud 

Habilita la sincronización iCloud en preferencias y en tus favoritos, marcadores y en el progreso en las sesiones sera sincronizado en todas tus Macs.

## Compartir

Puedes facilmente compartir links a las sesiones o videos usando el boton de compartir. los links compartidos son links universales que reedirigen al sitio de desarrolladores de Apple, para que si son abiertos en una Mac que tenga la app instalada, abrirán en la app. Los links también son compatibles con dispositivos iOS usando la aplicación Apple Developer

## Nerdy bits 🤓

### Code of Conduct
Esperamos que todos nuestros contribuyentes ayuden a mantener los valores establecidos en nuestro [codigo de conducta](./CODE_OF_CONDUCT.md). Creemos fundamentalmente que esto nos ayudará a construir una mejor comunidad y, con ella, una mejor aplicación.

### Contribuciones

Por favor lea [pautas de contribución](CONTRIBUTING.md) antes de abrir un issue o un pull request.

### Librarias externas

La aplicación utiliza varias bibliotecas de terceros:

- [Realm](https://realm.io): almacenamiento de datos y caché
- [Sparkle](https://sparkle-project.org/): actualizaciones automáticas 
- [CloudKitCodable](https://github.com/insidegui/CloudKitCodable): soporte de sincronización
- [Siesta](http://bustoutsolutions.github.io/siesta/): redes 
- [RxSwift](https://github.com/ReactiveX/RxSwift):  extensiones reactivas
- [RxRealm](https://github.com/RxSwiftCommunity/RxRealm): extensiones reactivas para Realm

### Librarias internas

- **ConfCore** es el núcleo de la aplicación que se ocupa de la API WWDC de Apple, almacenamiento de datos, almacenamiento en caché, sincronización y transcripciones (todo lo que tiene que ver con los datos, básicamente)
- **ConfUIFoundation** contiene colores compartidos, definiciones de fuentes y otras extensiones útiles utilizadas por el main app target y el `PlayerUI`
- **PlayerUI** contiene los componentes de la interfaz de usuario para el reproductor de video y algunos componentes de la interfaz de usuario de uso general utilizados en toda la aplicación
- **ThrowBack** proporciona soporte para la migración de datos de usuario y preferencias de versiones anteriores de la aplicación

## Compilando la aplicación

**Compilación requiere Xcode 11.5 or superior.**

Compilar la app requiere instalar [Carthage](https://github.com/Carthage/Carthage) 

**Clona esta rama y antes de abrir el proyecto, corre `./bootstrap.sh`** para buscar las dependecias (este script puede tardar mientras corre, es normal).

Como la app usa CloudKit,
Since the app uses CloudKit, cuando la compilas tu mismo, todas las funcionalidades dependientes de CloudKit no estarán disponibles. CloudKit requiere un provisioning profile y una cuenta de desarrollador de pago.

Para compilar la app tu mismo sin la necesidad de una cuenta de desarrollador y el contenedor CloudKit
To build the app yourself without the need for a developer account and a CloudKit container, **siempre usa la `WWDC` target al compilar**. La `WWDC with iCloud` target requiere una cuenta de desarrollador paga y un contenedor CloudKit, que no podrá crear debido al identificador de paquete de la aplicación.

![schedule](./screenshots/v7/BuildTarget.png)

### Borrar datos de la aplicación durante el desarrollo

Si necesita borrar las preferencias de la aplicación y los datos almacenados durante el desarrollo, puede ejecutar `./cleardata.sh` en la carpeta del proyecto. **Esto eliminará todas sus preferencias y datos como favoritos, marcadores y progreso en videos, así que tenga cuidado**.


# The unofficial WWDC app for macOS 

Enjoy WWDC from the comfort of your Mac with the unofficial WWDC app for macOS. Whether you're (virtually) attending or not, you can access livestreams, videos and sessions during the conference and as a year-round resource.

In partnership with CocoaHub, you can also use the app's Community tab to browse through Apple announcements, updates to the Swift language, new episodes from your favorite podcasts, community blog posts, and more.

⬇️ If you just want to download the latest release, go to [the website](https://wwdc.io).

## Schedule

The schedule tab shows the schedule for the current edition of WWDC, and allows you to watch live streams for the Keynote and other sessions throughout the week.

## Videos

Watch this year's videos as they're released and access videos from previous years. You can also read transcripts of sessions and easily jump to a specific point in the relevant video. Transcripts are also searchable and available in

![videos](./screenshots/v7/Transcript.png)

### Video features

- Watch videos in 0.5x, 1x, 1.25x, 1.5x, 1.75x or 2x speeds
- Fullscreen and native picture-in-picture support
- Navigate video contents easily with the help of transcripts

### Clip Sharing

Clip Sharing allows you to share a short segment (up to 5 minutes) from a session's video. This is a great feature for quickly sharing snippets of content from the conference.

![clipsharing](./screenshots/v7/ClipSharing.png)

## Chromecast

You can watch WWDC videos (both live and on-demand) on your Chromecast. Just click the Chromecast button while playing a video, choose your device from the list and control playback using the Google Home app on your phone.

![chromecast](./screenshots/v7/ChromeCast.png)

## Bookmarks

Have you ever found yourself watching a WWDC session and wishing you could take notes at a specific point in the video to refer back to later on? This is now possible with bookmarks.

With bookmarks, you can create a reference point within a video and add an annotation to it. Your bookmark annotations can also be considered while using the search, so it's easier than ever to find the content you've bookmarked before.

![bookmarks](./screenshots/v7/Video-Bookmark.png)

## Community

Browse content curated by the [CocoaHub](http://cocoahub.app) team in the Community tab.

![community](./screenshots/v7/Community.png)

## iCloud Sync

Enable the iCloud sync in preferences and your favorites, bookmarks and progress in sessions will be synced accross your Macs.

## Sharing

You can easily share links to sessions or videos by using the share button. The links shared are universal links that redirect to Apple's developer website, so if they're opened on a Mac which has the app installed, they will open in the app. The links are also compatible with iOS devices using the Apple Developer app.

## Nerdy bits 🤓

### Code of Conduct
We expect all of our contributors to help uphold the values set out in our [code of conduct](./CODE_OF_CONDUCT.md). We fundamentally believe this will help us build a better community, and with it a better app.

### Contributing

Please read the [contribution guidelines](CONTRIBUTING.md) before opening an issue or pull request.

### External libraries

A number of third-party libraries are used by the app:

- [Realm](https://realm.io): data storage and caching
- [Sparkle](https://sparkle-project.org/): automatic updates
- [CloudKitCodable](https://github.com/insidegui/CloudKitCodable): sync support
- [Siesta](http://bustoutsolutions.github.io/siesta/): networking
- [RxSwift](https://github.com/ReactiveX/RxSwift): reactive extensions
- [RxRealm](https://github.com/RxSwiftCommunity/RxRealm): reactive extensions for Realm

### Internal libraries

- **ConfCore** is the core of the app that deals with Apple's WWDC API, data storage, caching, syncing and transcripts (everything that has to do with data, basically)
- **ConfUIFoundation** contains shared color, font definitions and other useful extensions used by the main app target and `PlayerUI`
- **PlayerUI** contains the UI components for the video player and some general-purpose UI components used throughout the app
- **ThrowBack** provides support for migration of user data and preferences from old versions of the app

## Building the app

**Building requires Xcode 11.5 or later.**

Building the app requires [Carthage](https://github.com/Carthage/Carthage) to be installed.

**Clone this branch and before opening the project, run `./bootstrap.sh`** to fetch the dependencies (this script can take a while to run, that's normal).

Since the app uses CloudKit, when you build it yourself, all of the CloudKit-dependant functionality will not be available. CloudKit requires a provisioning profile and a paid developer account.

To build the app yourself without the need for a developer account and a CloudKit container, **always use the `WWDC` target when building**. The `WWDC with iCloud` target requires a paid developer account and a CloudKit container, which you won't be able to create because of the app's bundle identifier.

![schedule](./screenshots/v7/BuildTarget.png)

### Clearing app data during development

If you need to clear the app's preferences and stored data during development, you can run `./cleardata.sh` in the project folder. **This will delete all of your preferences and data like favorites, bookmarks and progress in videos, so be careful**.
