# Mixed Reality Museum Navigation Application

Museum Exploration MR is a Unity application for exploring the cultural heritage of Terengganu on Meta Quest. Visitors use a wrist menu or scan exhibit QR codes to open galleries, inspect 3D artifacts, and explore historical stories while seeing their physical surroundings through headset passthrough.

## What visitors can explore

- **Four galleries** cover textiles in Galeri Tekstil, performing arts in Galeri Seni, the Batu Bersurat Terengganu inscription in Serambi Mandalika, and traditional crafts in Galeri Kraf.
- **Artifact exhibits** combine rotatable 3D models, photographs, and Malay and English narration. Featured artifacts include Kain Songket, Gamelan Terengganu, and Batu Bersurat Terengganu.
- **Sejarah Terengganu** presents historical stories through narrated photos and short video clips.
- **Three mini-games** challenge visitors to identify artifact silhouettes, sequence the steps of batik making, and order historical events. Scores are stored locally, with cloud rankings backed by Firestore.
- **Hand and controller interactions** include pinch selection, artifact rotation, and a wrist menu for switching galleries and opening exhibits.

## Run the project

You need Unity **2022.3.39f1**, Git LFS, and Android Build Support with the Android SDK, NDK, and OpenJDK. To test on a Meta Quest headset, enable Developer Mode and connect it by USB.

1. Clone the repository and download the media assets.

   ```bash
   git lfs install
   git clone https://github.com/NelsenKeane/Mixed-Reality-Museum-Navigation-Application.git
   cd Mixed-Reality-Museum-Navigation-Application
   git lfs pull
   ```

2. Add the cloned folder to Unity Hub and open it with Unity 2022.3.39f1. Let Unity restore the packages from [Packages/manifest.json](Packages/manifest.json).
3. Open [Assets/Scenes/1.unity](Assets/Scenes/1.unity). In **File > Build Settings**, switch to **Android** and confirm that this scene is enabled.
4. In **Edit > Project Settings > XR Plug-in Management**, check the Android **OpenXR** and **Meta Quest Support** settings. Select the connected headset under **Run Device**, then choose **Build And Run**.

## Editor tools

- **Tools > Museum MR > Room & Artifact Data Manager** edits exhibit records and their media assignments.
- **Tools > Museum MR > QR Code Generator** creates printable codes for rooms and artifacts.
- In Play Mode with `QRCodeScannerDebugger` enabled, keys `1`–`5` simulate room scans, `6`–`8` simulate artifact scans, and `X` simulates losing sight of a QR code.

## Project layout

| Path | Contents |
| --- | --- |
| [Assets/Scenes](Assets/Scenes) | Main museum scene and test scenes |
| [Assets/Script](Assets/Script) | Navigation, interactions, exhibit panels, mini-games, and Editor tools |
| [Assets/Resources/MuseumData](Assets/Resources/MuseumData) | Room and artifact data |
| [Packages](Packages) and [ProjectSettings](ProjectSettings) | Unity dependencies and XR build configuration |

## Credits

The exhibits draw on the collections and historical material of Lembaga Muzium Negeri Terengganu (Terengganu State Museum, Malaysia). Batu Bersurat Terengganu is recognized by the UNESCO Memory of the World programme.

This repository is based on [the Museum Exploration MR project](https://github.com/wilymanhoward/Museum-Exploration-MR).
