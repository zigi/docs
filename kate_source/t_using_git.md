# Using Git

This topic explains how to use Git.

1.  Create an account at GitHub.com, and then add your \(Mainframe\) SSH Public Key to your account.

2.  If you have not added your SSH keys to your GitHub settings, provide your username and password at the prompt.

    It is highly recommended that you add your public SSH key to your GitHub account settings to eliminate the prompts for userid and password.

3.  Sign into OMVS, and then change to the directory where you are installing ZIGI.

4.  Do one of the following:

    -   If your SSH key is already generated and added to your GitHub account, execute the following command:

        ```
        git clone git@github.com:wizardofzos/zigi.git
        cd zigi
        sh install.sh
        ```

    -   If you haven’t added your SSH key to Github clone via https, execute the following command:

        ```
        git clone https://github.com/wizardofzos/zigi.git
        [provide GitHub username and password when prompted]
        cd zigi
        sh install.sh
        ```

        *NEXT TOPIC*: [Additional Options](r_additional_options.md)


-   **[Additional Options](r_additional_options.md)**  
This topic provides an overview on how to download ZIGI from the internet, unzip the files, upload the files to your mainframe, and then run the installer if you're unable to connect your mainframe to GitHub.

**Parent topic:**[Installing ZIGI](c_installing_zigi.md)

