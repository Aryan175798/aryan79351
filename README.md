candidate1=input("Enter 1st candiate name:")
candidate2=input("Enter 2nd candiate name:")
candidate1_votes=0
candidate2_votes=0
voters_id=[101,102,103,104,105,106]
no_of_voters=len(voters_id)
print("number of voters:",no_of_voters)
voted=[]
while True:
    if voters_id==[]:
        print("voting is over")
        if candidate1_votes>candidate2_votes:
            print(f"{candidate1} won the election with {candidate1_votes}")
        elif candidate2_votes>candidate1_votes:
            print(f"{candidate2} won the election with {candidate2_votes}")
        elif candidate1_votes==candidate2_votes:
            print("tied!!!")
        break

    else:
        voter=int(input("Enter your id"))
        if voter in voted:
            print("You already Voted")
        else:
            if voter in voters_id:
                print(f"1.{candidate1}\n2.{candidate2}")
                choice=int(input("Enter your choice"))
                if choice==1:
                    candidate1_votes+=1
                    print(f"you voted {candidate1}")
                elif choice==2:
                    candidate2_votes+=1
                    print(f"you voted {candidate2}")
                voters_id.remove(voter)
                voted.append(voter)
            else:
                print("you are not allowed to vote") 
#update by aryan
