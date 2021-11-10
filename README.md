# Tugas-Praktikum-4-Pointer-Project-based-
Oct 18, 2021

Buatlah sebuah program dengan bahasa C dengan ketentuan di bawah ini:

1. Memuat definisi dan pemanggilan fungsi buatan sendiri yang memungkinkan pass-by-reference (dalam kata lain, menerima argumen berupa pointer)
2. Melibatkan manipulasi variabel yang terletak di luar scope fungsi tersebut


        #include <stdio.h>
        #include <stdlib.h>
        #include <time.h>

        int level()
        { srand (time(NULL));
            int x;
                x = rand() %5 + 1;
                return x;
        }
        int vsBoss (int *healthPtr, int Hboss );
        int main (){
            int health = 0;

            printf ("Anda Mencapai Level %i ", level());

            if (level() == 1) {
                health = 20;
            }
            else if (level() == 2) {
                health = 40;
            }
            else if (level() == 3) {
                health = 60;
            }
            else if (level() == 4) {
                health = 80;
            }
            else if (level() == 5) {
                health = 100;
            }

        printf ("\nHP Anda Adalah : %i", health);

        printf ("\n\n==========Fight==========\n\n");
        int starBoss;
        printf ("Pilih Boss Yang Akan Dilawan\n1. Leviathan (1 Star Boss)\n2. Dexter (2 Star Boss)\n3. Cynthia (3 Star Boss)\n4. Wildkin (4 Star Boss)\n5. Titan (5 Star Boss)\n6. Gildan (6 Star Boss)\n7. Frosty Ace (7 Star Boss)\n8. Minerva (8 Star Boss)\n9. Neritha (9 Star Boss)\n10. Athena (10 Star Boss)\n\n\nPilihan : ");
        scanf ("%i", &starBoss);

        if (starBoss == 1){
                printf ("Kamu Sedang Melawan Leviathan");
            vsBoss(&health, 10);
        }
        else if (starBoss == 2){
                printf ("Kamu Sedang Melawan Dexter");
            vsBoss(&health, 20);
        }
        else if (starBoss == 3){
                printf ("Kamu Sedang Melawan Cynthia");
            vsBoss(&health, 30);
        }
        else if (starBoss == 4){
                printf ("Kamu Sedang Melawan Wildkin");
            vsBoss(&health, 40);
        }
        else if (starBoss == 5){
                printf ("Kamu Sedang Melawan Titan");
            vsBoss(&health, 50);
        }
        else if (starBoss == 6){
                printf ("Kamu Sedang Melawan Gildan");
            vsBoss(&health, 60);
        }
        else if (starBoss == 7){
                printf ("Kamu Sedang Melawan Forsty Ace");
            vsBoss(&health, 70);
        }
        else if (starBoss == 8){
                printf ("Kamu Sedang Melawan Minerva");
            vsBoss(&health, 80);
        }
        else if (starBoss == 9){
                printf ("Kamu Sedang Melawan Neritha");
            vsBoss(&health, 90);
        }
        else if (starBoss == 10){
                printf ("Kamu Sedang Melawan Athena");
            vsBoss(&health, 99);
        }
        else {printf("Maaf Boss Tidak Diketahui");}

        if (health <= 0){
            printf ("\n\n=======Defeat=======\n\n");
        }
        else if (health > 0){
            printf("\n\n=======Victory=======\nSisa HP : %i\n\n", health);
        }
        return 0;
        }
        int vsBoss (int *healthPtr, int Hboss ) {
            *healthPtr = *healthPtr - Hboss;
        }
