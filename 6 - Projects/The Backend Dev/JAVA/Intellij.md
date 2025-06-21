Java IDE of choice for Dan; what I'm learning on.

---
### 🛠️ **Install IntelliJ IDEA on Desktop (Ultimate Edition .tar.gz)**

#### 📦 1. **Extract the Archive**

Let’s assume the archive is at:

```
~/Desktop/ideaIU-2025.1.1.1.tar.gz
```

Run in terminal:

```bash
cd ~/Desktop
tar -xzf ideaIU-2025.1.1.1.tar.gz
```

This will create a folder like:

```
idea-IU-2025.1.1.1/
```

We'll refer to that as your `{installation home}`.

---

#### 🚀 2. **Start IntelliJ IDEA**

```bash
cd ~/Desktop/idea-IU-2025.1.1.1/bin
./idea.sh
```

> This initializes config files in:
> 
> - `~/.config/JetBrains/IdeaIC2025.1`
>     
> - `~/.local/share/JetBrains/IdeaIC2025.1`
>     

---

### ⚙️ **Step 3 – Add IntelliJ to PATH**

This allows you to launch IntelliJ IDEA from any terminal using `idea.sh`.

#### ✅ Terminal Instructions:

Run the following command to add IntelliJ’s `bin` folder to your shell’s `$PATH`:

```bash
echo 'export PATH="/home/elryan/Apps/idea-IC-251.26094.121/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

> If you’re using Zsh instead of Bash, replace `~/.bashrc` with `~/.zshrc`.

### 🧪 Test It

After that, you should be able to launch IntelliJ from anywhere with:

```bash
idea.sh
```

Or directly run:

```bash
/home/elryan/Apps/idea-IC-251.26094.121/bin/idea.sh
```

---

#### 🧠 4. **[Optional] Customize JVM Heap Size**

Create a config file if you want to tweak memory usage:

```bash
mkdir -p ~/.config/JetBrains/IdeaIC2025.1
cp ~/Desktop/idea-IU-2025.1.1.1/bin/idea64.vmoptions ~/.config/JetBrains/IdeaIC2025.1/idea64.vmoptions
```

Then edit it:

```bash
nano ~/.config/JetBrains/IdeaIC2025.1/idea64.vmoptions
```

Change values like:

```text
-Xms512m
-Xmx4096m
```

---

#### 📁 5. **[Optional] Change Config & Cache Directories**

If you want to store config/system files elsewhere:

```bash
mkdir -p ~/custom/idea-config
mkdir -p ~/custom/idea-system
nano ~/.config/JetBrains/IdeaIC2025.1/idea.properties
```

Add:

```
idea.config.path=~/custom/idea-config
idea.system.path=~/custom/idea-system
```

---

#### 🖥️ 6. **[Optional] Create Desktop Entry**

```bash
nano ~/.local/share/applications/intellij-idea.desktop
```

Paste this:

```ini
[Desktop Entry]
Version=1.0
Type=Application
Name=IntelliJ IDEA Ultimate
Exec=/home/landondahle/Desktop/idea-IU-2025.1.1.1/bin/idea.sh
Icon=/home/landondahle/Desktop/idea-IU-2025.1.1.1/bin/idea.png
Terminal=false
Categories=Development;IDE;
```

Then:

```bash
chmod +x ~/.local/share/applications/intellij-idea.desktop
```

---

