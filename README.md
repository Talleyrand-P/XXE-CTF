# XXE-CTF
A small XXE CTF using a vulnerable PHP script.

To download the code use the command

```git clone https://github.com/Talleyrand-P/XXE-CTF```

Make sure you have docker installed, navigate to the XXE-CTF directory and run the following command

```docker build .```

```docker run -p 8080:80 <the_id_from_build>```

The CTF will now be running. You can access it by going to

```http://0.0.0.0:8080/register.html```

To stop it once you are finished use the below commands

```docker ps```

```docker stop <containter_id_of_the_CTF>```
