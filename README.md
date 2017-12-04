# help-nee-fixing-
help fix my code


#include <iostream>
#include <string>
#include <cstdlib>
#include <stdlib.h>

using namespace std;

int enemy_exp_give = 15;
int player_level = 1;
int player_exp = 0;
int player_next_level = 50;
int gold = 0;
int player_role;
int player_name;
int player_id;
int player_heath = 100;
int player_mp = 100;
int player_stat;
int enemy_heath = 100;
int choice;
int choice_two;
int backstab_number[10];
int mage_stats[6] = {100,100,25,55,30,25};
int tank_stats[6] = {200,125,50,25,25,25};
int support_stats[6] = {150,150,100,50,50,25};
bool bleed = false;
bool poisin = false;
bool burn = false;
bool freeze = false;
bool paralysis = false;
bool sleep = false;
bool bound = false;
bool confusion = false;
void battle();
void inn();
void forest();
void castle();
void castle_gate();
void intro();
void game();
void your_character();
void town_center();
void blacksmith();
void alchemy_shop();
void spell_shop();
void shops();
void pick_class();
void town_quest_board();

void pick_class()
{
    cout << "this is a fan made text based game based on the dark souls series" << endl;
    cout << "so of you like it tell your friends about it to so lets play the game" << endl;
    cout << "pick a class" << endl << "1.mage" << endl << "2.tank" << endl << "3.support" << endl;
    cout << "class:"; cin >> choice;

    switch(choice)
    {
        case 1:
            player_id = 1;
                your_character();
                    break;

        case 2:
            player_id = 2;
                your_character();
                    break;

        case 3:
            player_id = 3;
                your_character();
                    break;

        default:
            system("CLS");
            pick_class();
                break;
    }
}

void your_character()
{
    switch(player_id)
    {
     case 1:
      cout << "Mage's stats:" << "HP=" << mage_stats[0] << " Stamina=" << mage_stats[1] << " Strength=" << mage_stats[2] << " intelligence=" << mage_stats[3] << " Faith=" << mage_stats[4] << " Dexterity=" << mage_stats[5] << endl;
            intro();
                break;


      case 2:
       cout << "  your role is a tank" << endl;
        cout << "Tank's stats:" << "HP=" << tank_stats[0] << " Stamina=" << tank_stats[1] << " Strength=" << tank_stats[2] << " intelligence=" << tank_stats[3] << " Faith=" << tank_stats[4] << " Dexterity=" << tank_stats[5] << endl;
            intro();
                break;

      case 3:
       cout << "  your role is a support" << endl;
        cout << "Support's stats:" << "HP=" << support_stats[0] << " Stamina=" << support_stats[1] << " Strength=" << support_stats[2] << " intelligence=" << support_stats[3] << " Faith=" << support_stats[4] << " Dexterity=" << support_stats[5] << endl;
            intro();
                break;

    }
}
void intro()
{

    cout << endl;
    cout << "   in this world everyone born with a role and the role your born with is the one you keep for life." << endl;
    cout << "but your special you get to put a role in the world so this is where your journey" << endl;
    cout << "your awake in a inn your don't remember anything from the fall off the chill" << endl;
    cout << "the inn keeper asked 'whats your name' name what is my name" << endl;
    cout << "Name: "; cin >> player_name;
    cout << "so your name is " << 'player_name' << endl;
    cout << "the inn keeper said 'you may find something at the castle'" << endl;
    gold += 100;
    cout << "you find 100 gold in you pocket ,so you leave the inn and go to the town center" << endl;
    castle_gate();
}

void town_center()
{
    cout << "your at the center of town and you see a sign that says" << endl;
    cout << "1.North-Inn  2.South-Shop  3.East-Castle Gate  4.Wast-Forest" << endl;
    cout << "what to do:"; cin >> choice; cout << endl;

    switch(choice)
    {
    case 1:
        inn();
        break;
    case 2:
        shops();
        break;
    default:
        shops();
        break;
    }

}


void shops()
{
    cout << "Welcome to the shops" << endl;
    cout << "Gold:"<< gold << endl;
    cout << "what do you want to buy" << endl;
    cout << "1.Blacksmith "; cout << " 2.Alchemy Shop "; cout << " 3.Spell Shop" << endl;
    cin >> choice;

    switch(choice)
    {
    case 1:
        blacksmith();
        break;
    case 2:
        alchemy_shop();
        break;
    case 3:
        spell_shop();
        break;

    }
}
void inn()
{
    cout << "Welcome back" << endl;
}
void forest()
{
    cout << "your on your way in the forest and you see a sign that says" << endl;
    cout << "'monster passed this point be ready to fight'are you ready then move forward" << endl;

}
void castle_gate()
{
    cout << "you go up to the castle's gate and see a guard" << endl;
    if (player_level < 10)
    {
        cout << "Guard:You look weak come back when your bigger" << endl;
        cout << "you feel bad so you go back to the town center" << endl;
        town_center();
    }else if (player_level >= 10)
    {
        cout << "go in the king looking for people like you" << endl;
        castle();
    }
}
void castle()
{

}
void blacksmith()
{

}

void alchemy_shop()
{

}

void spell_shop()
{

}

int main()
{
    pick_class();
    return(0);
}
