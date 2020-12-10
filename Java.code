package com.company;

import java.util.Scanner;

import static java.lang.Math.round;

public class Main {

    public static void main(String[] args) {
        // write your code here
        Scanner input = new Scanner(System.in);
        System.out.print("Let me hear sum: ");
        String usertext = input.nextLine();
        float words = 1;
        float sentences = 0;
        float letters = 0;

        //checks if a character is a letter


        for (int i = 0; i < usertext.length(); i++) {
            if (Character.isLetter(usertext.charAt(i))) {
                letters++;
            }
        }

        //checks to see if it is a word
        for (int i = 0; i < usertext.length(); i++) {
            if (Character.isSpaceChar(usertext.charAt(i))) {
                words++;
            }
        }

        //checks to see # of sentences
        for (int i = 0; i < usertext.length(); i++) {
            if (usertext.charAt(i) == '.' || usertext.charAt(i) == '?' || usertext.charAt(i) == '!') {
                sentences++;
            }
        }


//coleman index formuula
        float level = ((letters / words) * 100);
        float sentence = ((sentences / words) * 100);
        float index = round(0.0588 * level - 0.296 * sentence - 15.8);

        if (index < 16 && index > 1) {
            System.out.println("Grade " + Math.round(index));
        }
        if (index >= 16) {
            System.out.println("Grade 16+");
        }
        if (index < 1) {
            System.out.println("Before Grade 1");
        }
    }
}
