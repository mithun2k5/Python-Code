#Ceasar Cipher,both encoding and decoding,for key value 1 to 25:

def ceasar_cipher():
    encryption=''"
    decryption=''"
    while not (encryption.lower()=='yes' or encryption.lower()=='no'):
        encryption = raw_input("Want to do encryption on text?(Yes or No): ")
    if (encryption.lower()=="yes"):
        text = raw_input('Enter text for encryption ')
        key = raw_input('Give key value(1-25): ')
        if int(key)<=25 and int(key)>=0:
            length = len(text)
            i=0
            lst='"'
            while (i<length):
                encrypted_value = ord(text[i])+int(key)
                if (encrypted_value >122):
                    encrypted_value = 96 + int(key)
                    lst = lst + chr(encrypted_value)
                else:
                    lst = lst + chr(encrypted_value)
                i=i+1
        else:
            return 'Invalid Key'
    else:
        while not (decryption.lower()=='yes' or decryption.lower()=='no'):
            decryption = raw_input("Want to do decryption on text?(Yes or No): ")
        if (decryption.lower()=='no'):
            message = "End of Program"
            return message
        else:   
            text = raw_input('Enter text for decryption ')
            key = raw_input('Give key value(1-25): ')       
            if int(key)<=25 and int(key)>=0:
                length = len(text)
                i=0
                lst=''
                while (i<length):
                    decrypted_value = ord(text[i])-int(key)
                    if (decrypted_value < 97):
                        decrypted_value = 123 - int(key)
                        lst = lst + chr(decrypted_value)
                    else:
                        lst =lst + chr(decrypted_value)
                    i=i+1
            else:
                return 'Invalid Key'
    print lst


ceasar_cipher()

Want to do encryption on text?(Yes or No): no
Want to do decryption on text?(Yes or No): yes
Enter text for decryption njuivo
Give key value(1-25): 1
mithun
