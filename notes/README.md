# Setup

Machine: Windows, PowerShell (IntelliJ terminal)

## Versions
| Tool | Version | Notes |
|---|---|---|
| JDK | Microsoft OpenJDK 25.0.5 | `C:\Users\lexib\.jdks\ms-25`, set as JAVA_HOME |
| IntelliJ IDEA | 2026.3 | |
| Gradle | ___ | from `gradle-wrapper.properties`, needs 9.1+ for Java 25 |
| Docker Desktop | ___ | `docker run hello-world` works |
| AWS CLI | ___ | installed via winget |
| Azure CLI | ___ | installed via winget |
| Terraform | ___ | installed via winget |
| Python | 3.11.9 | plan said 3.12; 3.11 is fine |

## Gotchas
- IntelliJ auto-downloaded JDK 27 for the new project. Switched to 25 in
  Project Structure (SDK + language level) and set Gradle JVM to Project SDK.
- VS Code's Java 25 is bundled with the extension, not on PATH.
  `where.exe java` shows what the terminal actually uses.
- In PowerShell use `where.exe`, not `where`.
- A `public class Main` must live in `Main.java` (case-sensitive).
- After installing CLIs or changing PATH/JAVA_HOME, fully restart IntelliJ.
- `git push` rejected with "fetch first" = remote has commits I don't have.
  Fix: `git pull --rebase origin main`.
- GitHub rulesets only enforce when Enforcement status = Active.
