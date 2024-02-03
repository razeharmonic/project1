#include <iostream>
using namespace std;



void chicken(){
std::cout << "------------- Chicken Menu -------------" << std::endl;
		cout << "		[1]Original Recipe Chicken (KFC)			55pesos" << endl;
		cout << "		[2]Chicken McNuggets (McDonald's))			85pesos" << endl;
		cout << "		[3]Chickenjoy (Jollibee))			        75pesos" << endl;
		cout << "		[4]Spicy Chicken Sandwich (Chick-fil-A))	92pesos" << endl;
}
void burger(){
 std::cout << "------------- Burger Menu -------------" << std::endl;
    std::cout << "[2] Classic Burger                            65 pesos" << std::endl;
    std::cout << "[3] Cheeseburger                              75 pesos" << std::endl;
    std::cout << "[4] Bacon Deluxe Burger                       85 pesos" << std::endl;
    std::cout << "------------------------------------------" << std::endl;
}
void drinks(){
	std::cout << "------------- Drinks Menu -------------" << std::endl;
    std::cout << "[1] Cola                                          25 pesos" << std::endl;
    std::cout << "[2] Lemonade                                      30 pesos" << std::endl;
    std::cout << "[3] Iced Tea                                      20 pesos" << std::endl;
    std::cout << "--------------------------------------------" << std::endl;
}
void fries(){
std::cout << "------------- Sides Menu -------------" << std::endl;
    std::cout << "            French Fries                                  40 pesos" << std::endl;
    std::cout << "  - [1] Regular                                   40 pesos" << std::endl;
    std::cout << "  - [2] Cheese                                    50 pesos" << std::endl;
    std::cout << "  - [3] Sour Cream and Onion                      45 pesos" << std::endl;
    std::cout << "  - [4] Barbecue                                  45 pesos" << std::endl;
    std::cout << "------------------------------------------" << std::endl;
}


int main(){
	  cout << "                     ------[1]--------       ------[2]------       ------[3]------     ------[4]-------     \n";
    cout << "                     | Fried Chicken |       |    burger   |       |    Drinks   |     | French Fries |     \n";
    cout << "                     -----------------       ---------------       ---------------     ----------------     \n";
    
    
    cout << "                     ------[5]-------       ------[6]------       ------[7]------      ------[8]------     \n";
    cout << "                     |    Snacks    |       |    Pizza    |       |    Tacos    |      |  Sandwiches |     \n";
    cout << "                     ----------------       ---------------       ---------------      ---------------      \n";
    
  
    cout << "                                   ------[9]-------      ----[10]----    ----[0]----      \n";
    cout << "                                   |  Reservation |      |  Receipt |    |   Exit  |         \n";
    cout << "                                   ----------------      -----------     -----------   \n";
    
	
	int choice;
	double totalcost;
	int quantity;
	int cost;
	do{
	

		cout<<"Enter ur category: " ;
		cin>>choice;
		
		switch(choice){
			case 1:
				chicken();
			
				break;
				case 2:
					burger();
					break;
				case 3:
					drinks();
					break;
					case 4:
						fries();
				cout<<"Enter Quantity: ";
				cin>>quantity;
				
				cost = totalcost * quantity;
						
					case 0:
						cout<<"Exit the Menu\n";
						break;
						default:
							cout<<"Invalid CHoice";
							
		}
		int itemchoice;
	char discount;
	double dis;
	double discounted;
		do{
			cout<<"Enter ur order: ";
			cin>>itemchoice;
			switch(choice){
				case 1:
					if(itemchoice == 1){
						totalcost += 55;
						//quantity 
								cout<<"Enter Quantity: ";
			                   	cin>>quantity;
				cost = totalcost * quantity;
				//discount
			cout<<"do you want to enter discount?: y for discount n forback";
			cin>>discount;
			
			if(discount =='y'){
				cout<<"Enter the discount: ";
				cin>>discounted;
dis = totalcost-(totalcost*discounted);
cout<<"Original Recipe Chicken (KFC) Added to ur order the total is "<<dis<<"\n";

			}else if(discount == 'n'){
					cout<<"Original Recipe Chicken (KFC) Added to ur order the total is "<<cost<<"\n";
			}

			
				
					
					}else if (itemchoice == 2){
						totalcost += 85;
						
						cout<<"Chicken McNuggets (McDonald's)) Added to ur order the total is "<<cost<<"\n";
					}else if (itemchoice == 3){
						totalcost += 75;
					;
						cout<<"Chickenjoy (Jollibee)) Added to ur order the total is "<<cost<<"\n";
					}else if(itemchoice == 4){
						totalcost +=75;
						
						cout<<"Spicy Chicken Sandwich (Chick-fil-A))tthe total is  "<<cost<<"\n";
					}
					break;
					case 0:
					cout<<"0 to Menu\n";
					break;
					default:
					cout<<"Invalid. try again";
			}
		}while(itemchoice != 0);
	}while(choice != 0);
}
