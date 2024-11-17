lab2.py
def main():
    print("ET0735 (devOps for AIoT) - lab 2 - Introduction to python")
    display_main_menu()
    num_list=get_user_input()
    calc_median_temperature(num_list)


def display_main_menu():
    print("Enter some numbers separated by commas: \n")

def get_user_input():
    str_list=input("enter value:")
    print("user_input ")
    split_list= str_list.split(",")
    fsplit_list = [float(value) for value in split_list]
    print(fsplit_list)
    return fsplit_list

def calc_average(fsplit_list):
    return sum(fsplit_list)/ len(fsplit_list)

def find_min_max(fsplit_list):
    return [min(fsplit_list), max(fsplit_list)]
    

def sort_temperature(fsplit_list):
    return sorted(fsplit_list)

def calc_median_temperature(fsplit_list):
    fsplit_list.sort()
    n=len(fsplit_list)

    if n % 2 == 1:
        median=fsplit_list[n // 2]

    else:
        pos1=fsplit_list[n // 2]
        pos2=fsplit_list[n // 2-1]
        median= (pos1+pos2)/2


    return median

if __name__ == "__main__":
    main()
