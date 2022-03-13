![image](https://user-images.githubusercontent.com/75273945/136714299-46e79596-24e0-4fcf-a864-ee8bf86faf6b.png)

<h4>This is a packet sniffer that will sniff several types of packets available to it and stores all the data of each packet in a text file
 <br>
Works only on Linux. 
 <br>
In the terminal, go to the folder with the files, enter make all and launch the program  "./packke_sniffer<h1>
 <br>
<h4>Program operation: <br>
1) We will start the process by opening a handler for the file that comes in. We will store all the information we "peeled" from the network traffic we read from our network card, we will use a FILE struct pointer to manage our file accesses.
 <br>
2) After creating the handler we will start our main function, we will create two variables, one was saddr_size and the other will be data_size, the first variable was responsible for storing let the socket size (in bytes), this will be necessary by peeling the information from the network traffic , The second variable will be used after extracting the information, the value of the variable was the same throughout the information received from the fact.
 <br>
3) We will create a pointer to a memory cell at the maximum size that a fact can be, this information will be taken what heap dynamically, can be seen by using the malloc function, after the dynamic planar pointer that comes back to us is void so we will make it kind of unsigned char because we do not want Cut the information into segments of different information units like 4 byte or 8 byte, we want the information in a way that reads byte by byte.
 <br>
4) We will use a pointer to the handler we created for the management of the log file to open a txt file. We use a function called fopen, for this function we pass two parameters, the desired file name and how to open it, we will use write ("W "), This type allows us to open a file and if it does not exist it will create one, assuming there is a file with this name it will delete all the stored information come and write come later, this function returns us the information needed to access the file, custom and after using this function Ask the handler in the test if it is equal to the value NULL, in case it is equal then the process of opening the file failed and should respond accordingly.
 <br>
5) We will create an int variable that will store the return value from the function that opens the socket, the value that is returned from this function is the socket descriptor, this is the number that the system uses to number and identify the sockets that it opens,
 <br>
6)We will start an infinite loop that comes we perform a number of operations
  <br>
7) We will close the socket we opened, in advanced systems as it exists today this thing happens with the end of program detection that opened sockets without closing them, but for backward compatibility and good habits we will close it manually and finish the program. 
 <br> 
 
 <h4>
