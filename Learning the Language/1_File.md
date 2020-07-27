# Read a file

- The file going to be read must be saved in the same directory as the python script used to open it.
- If the file is not saved in the correct directory, proper path measures must be taken, which will be covered later

      file = open('file.txt', 'r') ##r represents read mode

      f = file.readlines()

      print(f)

      myList = []

      for line in f:
          if line[-1]=='\n':
              myList.append(line[:-1])
          else:
              myList.append(line[:])

      print(myList)

      ##We may also use :

      myList.clear()

      for line in f:
          myList.append(line.strip())

      print(myList)
      
  #### file_name.close() is used to save the changes
  
  # Write in a file
  
  - Clear ups the existing file content and overwrites
  - This property can be changes, we'll get into that later.
  
  
        file = open('file.txt', 'w') ##w represents write mode

        file.write('I am a good boy\n')
        file.write('I am happpy')

        file.close() ##without this, nothing will be written, just blank file will be got
