## Installation of the program

Copy provided archive `boardtrix.tar` to desired directory. For example, to user's home directory (`/home/<User name>`).

### 1.
Open `Terminal` app and go to directory with copied `boardtrix.tar` archive:
```bash
cd <path to `boardtrix.tar` directory>
```

### 2.
Create `boardtrix` folder in the same directory:
```bash
mkdir boardtrix
```

### 3.
Unzip `boardtrix.tar` into the created directory:
```bash
tar -xf boardtrix.tar -C ./boardtrix
```
and go to it:
```bash
cd ./boardtrix
```

### 4.
If current user doesn't have superuser permissions, you can use `./install_sudo.sh` script in the same folder, run the command and follow appearing instructions to do this:
```bash
./install_sudo.sh
```
Reboot your PC after complete execution of the script.  

### 4.5.
If step `4` was completed, open terminal again after PC reboot and go to archive direсtory (repeat step `1`) and go straight to step `5`.

### 5.
Execute `update_source_list.sh` script to add repository with `boardtrix` packages to system repository list:
```bash
sudo ./update_source_list.sh
```

### 6.
Install program by running the command below and following the instructions that appear:
```
sudo apt install boardtrix
```

Installed program can be launched either by executing a command in the terminal (from any directory):
```bash
boardtrix
```
or using the tools of the desktop environment installed in the system (for example `GNOME` or `XFCE`), by searching in the application menu by the name of the program: `boardtrix`.

## Uninstalling of the program:

To remove the application, run the command in the terminal:
```bash
sudo apt autoremove boardtrix
```
