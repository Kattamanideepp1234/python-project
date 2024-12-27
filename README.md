# python-project
#email slicing using split method
def email_slicer_1(email):
    if '@' and '.' in email:
        username,domain=email.split("@")
        domain_name,domain_extension=domain.split(".",1)
        if len(username)==0 or len(domain_name)==0 or len(domain_extension)==0 or not domain_name.isalpha() or not domain_extension.isalpha():
            print("invalid email id")
        else:
            print("username:",username)
            print("domain_name:",domain_name)
            print("domain_extension:",domain_extension)   
    else:
        print("invaild email id")
        
#email slicing using index
def email_slicer_2(email):
    if '@' and '.' in email:
        index_1=email.index('@')
        index_2=email.index('.')
        if len(email[:index_1])==0 or len(email[index_1+1:index_2])==0 or len(email[index_2+1:])==0 or not email[index_1+1:index_2].isalpha() or not email[index_2+1:].isalpha() :
            print("invalid email id")
        else:
            print("username:",email[:index_1])
            print("domain_name:",email[index_1+1:index_2])
            print("domain_extension:",email[index_2+1:])
    else:
        print("invaild email id")
        
email=input("enter your email id for slicing:")
email_slicer_1(email)
email_slicer_2(email)
