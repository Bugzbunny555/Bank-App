# Bank-App
if name == "" or age == "" or gender == "" or password == "":
    notif.config(fg="red",text="All fields requried * ")
    return

for name_check in all_accounts:
    if name == name_check:
        notif.config(fg="red",text="Account already exists")
        return
    else:
        new_file = open(name,"w")
        new_file.write(name+'\n')
        new_file.write(password+'\n')
        new_file.write(age+'\n')
        new_file.write(gender+'\n')
        new_file.write('0')
        new_file.close()
        notif.config(fg="green", text="Account has been created")
