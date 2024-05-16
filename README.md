# Go-tutorial
Install Go on your MacBook using Homebrew, which is a package manager for macOS. Here's how you can do it:

1. **Install Homebrew** (if you haven't already):
   
   Open Terminal and paste the following command:

   ```
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

   Follow the on-screen instructions to complete the installation.

2. **Install Go using Homebrew**:
   
   Once Homebrew is installed, you can install Go by running the following command in Terminal:

   ```
   brew install go
   ```

   This will download and install the latest version of Go on your MacBook.


3. **Set up your Go workspace**:
   - Go expects your code to be organized in a specific directory structure called the workspace. The default workspace is typically located at `$HOME/go`. You can set this up by creating the directory if it doesn't exist:
     ```
     mkdir ~/go
     ```
   - Inside your Go workspace, you'll have three subdirectories:
     - `bin`: For executable binaries.
     - `pkg`: For compiled package objects.
     - `src`: For your Go source files.

4. **Set up your PATH**:
   - To make Go commands accessible from any terminal window, you need to add Go's bin directory to your PATH environment variable.
   - Open your terminal and edit your shell profile file. If you're using the default Terminal application, this is typically `~/.bash_profile` or `~/.zshrc` if you're using Zsh.
   - Add the following line to the file, replacing `$HOME` with the absolute path to your home directory:
     ```
     export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin
     ```
   - Save the file and then execute the command to apply the changes to your current terminal session:
     ```
     source ~/.bash_profile
     ```
     or
     ```
     source ~/.zshrc
     ```

5. **Verify your Go installation**:
   - Open a new terminal window and type:
     ```
     go version
     ```
   - You should see the installed Go version printed on the screen. This confirms that Go is successfully installed and configured on your MacBook.

