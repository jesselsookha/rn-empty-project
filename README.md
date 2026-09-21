# Empty Project – React Native / Expo Starter

## I. Purpose of this Repository
A small number of students have experienced errors when creating a new React Native project using:

```bash
npx create-expo-app -t expo-template-blank-typescript
```

To avoid these issues, this repository provides a ready‑made Expo TypeScript project. By cloning this repository, you can begin coding immediately without needing to generate a new project from scratch.

---

## II. Two Available Workflows

### A. Manual Workflow
1. **Clone the repository**  
   Use GitHub Desktop or run (in the terminal):  
   ```bash
   git clone <repo-url>
   ```

2. **Rename the folder**  
   Change `empty-project` to your chosen project name.

3. **Disconnect from the original repository**  
   Inside the project folder, run:  
   ```bash
   git remote remove origin
   ```

4. **Edit configuration files**  
   - In `app.json`:
     ```json
     {
       "expo": {
         "name": "empty-project",
         "slug": "empty-project",
         ...
       }
     }
     ```
     Change both `name` and `slug` to your chosen project name.

   - In `package.json`:
     ```json
     {
       "name": "empty-project",
       "version": "1.0.0",
       ...
     }
     ```
     Change `name` to your chosen project name.

5. **Install dependencies**  
   Run:
   ```bash
   npm install
   ```

6. **Begin coding**  
   Start the development server:
   ```bash
   npx expo start
   ```
   Scan the QR code with Expo Go on your phone (or follow emulator instructions discussed in class).

---

### B. Automated Workflow (Script)

To simplify the process, two scripts are available:

- [PowerShell script (`setup-project.ps1`)](https://gist.github.com/jesselsookha/38010f790b751f9920d8e374d4e63950)  
- [Batch script (`setup-project.bat`)](https://gist.github.com/jesselsookha/868fffdde279336e32b7055c654d82bc)  

Both scripts are designed to help you quickly create a personalised copy of the `empty-project` without needing to manually edit configuration files.

---

#### I. Placement of the Script
- The script must be placed **one level above** the `empty-project` folder.  
- Example directory structure:  
  ```
  Projects/
  ├── setup-project.ps1
  ├── setup-project.bat
  └── empty-project/
  ```
- This ensures the script can find and copy the `empty-project` folder correctly.

---

#### II. Executing the PowerShell Script
1. Open **PowerShell**.  
2. Navigate to the folder containing the script and the `empty-project` folder:  
   ```powershell
   cd C:\Users\Student\Projects
   ```
3. Run the script:  
   ```powershell
   .\setup-project.ps1
   ```
4. When prompted, type your new project name (e.g., `student-app`).  
5. The script will:  
   - Copy the `empty-project` folder into a new folder with your chosen name.  
   - Update `app.json` (`name`, `slug`).  
   - Update `package.json` (`name`).  
   - Remove the GitHub remote connection (`git remote remove origin`).  
6. Navigate into your new folder and run:  
   ```powershell
   npm install
   ```
   This restores the `node_modules` folder.

---

#### III. Executing the Batch Script
1. Open **Command Prompt**.  
2. Navigate to the folder containing the script and the `empty-project` folder:  
   ```cmd
   cd C:\Users\Student\Projects
   ```
3. Run the script:  
   ```cmd
   setup-project.bat
   ```
4. When prompted, type your new project name (e.g., `student-app`).  
5. The script will:  
   - Copy the `empty-project` folder into a new folder with your chosen name.  
   - Remove the GitHub remote connection (`git remote remove origin`).  
   - **Note:** Batch scripts cannot automatically edit JSON files. You must manually update `app.json` and `package.json`:
     - In `app.json`, change:
       ```json
       "name": "empty-project",
       "slug": "empty-project"
       ```
       to your chosen project name.  
     - In `package.json`, change:
       ```json
       "name": "empty-project"
       ```
       to your chosen project name.  
6. Navigate into your new folder and run:  
   ```cmd
   npm install
   ```

---

#### IV. After Running Either Script
- Open the new project folder in VS Code.  
- Run:
  ```bash
  npx expo start
  ```
  Scan the QR code with Expo Go to view your app.  
- Edit the README to describe your own project.  
- Install additional dependencies as needed (navigation, async storage, image picker, etc.).

---

## III. Next Steps After Setup
1. **Edit the README**  
   Replace this content with details about your own project.

2. **Install additional dependencies**  
   For example:
   ```bash
   npx expo install @react-navigation/native
   npx expo install @react-native-async-storage/async-storage
   npx expo install expo-image-picker
   ```
   Use `npx expo install` for Expo/React Native packages, and `npm install` for general JavaScript libraries.

3. **Run your project**  
   ```bash
   npx expo start
   ```
   Scan the QR code with Expo Go to view your app.

---

## IV. Summary
- This repository exists to provide a stable starting point for React Native projects.  
- You may either **manually edit** the configuration files or use the **automation scripts** to personalise your project.  
- Once configured, install dependencies and begin coding.  
- Always update the README to reflect your own work.
