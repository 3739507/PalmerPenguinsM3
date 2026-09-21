# PalmerPenguinsM3
// PalmerPenguinsM3.java
// Donny Nelson
// 09/13/2026
// This program to calculate and display Palmer Penguin statistics

import java.util.Scanner;


public class PalmerPenguinsM3 {

   
        static final String SP_CHINSTRAP = "Chinstrap";
        static final String SP_GENTOO = "Gentoo";
        static final String SP_ADELIE = "Adelie";
      
        static final int NUM_CHINSTRAP = 68;
        static final int NUM_GENTOO = 123;
        static final int NUM_ADELIE = 151;
        
        static final int TOTAL_SPECIES = 3;
        static final int PENGUINS_IN_DATABASE = 342;
        
       
        public static void main(String[] args) {
        
        Scanner scnr = new Scanner(System.in);
                 
        String chosenSpecies;
        
        int totalPenguins = NUM_CHINSTRAP + NUM_GENTOO + NUM_ADELIE;
        
         System.out.println ("Introducing the Palmer Penguins: ");
         System.out.println ("\t" + SP_CHINSTRAP + "!");
         System.out.println ("\t" + SP_GENTOO + "!");
         System.out.println ("and last but not least...");
         System.out.println ("\t" + SP_ADELIE + "!");
         System.out.println ("There are a total of " + TOTAL_SPECIES + " penguin species in this dataset.");
         System.out.println ("There are a total of " + PENGUINS_IN_DATABASE + " penguins in the dataset");
         System.out.printf ("%s: %d (%.2f%%)\n", SP_CHINSTRAP, NUM_CHINSTRAP, (double) NUM_CHINSTRAP / totalPenguins * 100);
         System.out.printf ("%s: %d (%.2f%%)\n", SP_GENTOO, NUM_GENTOO, (double) NUM_GENTOO / totalPenguins * 100);
         System.out.printf ("%s: %d (%.2f%%)\n", SP_ADELIE, NUM_ADELIE, (double) NUM_ADELIE / totalPenguins * 100);
         System.out.printf ("\n");
         System.out.printf ("Branching Analysis: \n");
         if(NUM_CHINSTRAP > NUM_GENTOO && NUM_CHINSTRAP > NUM_ADELIE){
            System.out.printf (SP_CHINSTRAP + " penguins are the most populus.");
            }
            else if (NUM_GENTOO > NUM_CHINSTRAP && NUM_GENTOO > NUM_ADELIE){
               System.out.printf (SP_GENTOO + " penguins are the most populus.");
               } else if (NUM_ADELIE > NUM_CHINSTRAP && NUM_GENTOO < NUM_ADELIE){ 
                    System.out.printf (SP_ADELIE + " penguins are the most populus.");
                     } else {
                        System.out.printf ("There is a tie between species for the most populus.");
                        }
         System.out.print ("\n");
         System.out.print ("\n");
         
         chosenSpecies = scnr.next();
         switch (chosenSpecies){
             case SP_CHINSTRAP: 
               System.out.printf ("%s: %d (%.2f%%)\n", SP_CHINSTRAP, NUM_CHINSTRAP, (double) NUM_CHINSTRAP / totalPenguins * 100);
               break;
             case SP_GENTOO: 
               System.out.printf ("%s: %d (%.2f%%)\n", SP_GENTOO, NUM_GENTOO, (double) NUM_GENTOO / totalPenguins * 100);
               break;
             case SP_ADELIE: 
               System.out.printf ("%s: %d (%.2f%%)\n", SP_ADELIE, NUM_ADELIE, (double) NUM_ADELIE / totalPenguins * 100);
               break;
              default:
               System.out.printf("Species not recognized.");
               break;
         }    
   
     }
      
      }
