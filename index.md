__Less Command in Linux__
> The "less" command in Linux is a powerful utility used for viewing and navigating through text files. It is often used as an alternative to the "more" command and offers additional features such as the ability to move both forwards and backwards within the file, search for text, and perform other advanced operations.
——————————————————————————————————————————————————————————————————
``` Example ```
——————————————————————————————————————————————————————————————————

__Command Line Options__ 
>-jn or --jump-target=n
>-n or --line-numbers
>
>

__-jn or --jump-target=n__
> The -j command option allows you to jump to a specific target line as specified by the variable 'n' in the command. The number specified starts from the first line at 1, but can also be used to jump from the back by using negative numbers as inputs, with -1 being the last line. Additionally, decimal numbers can be used to travel a perentage of the screen down, with .3 being 30% down and .5 being half down.
——————————————————————————————————————————————————————————————————
> setting 8 as the value for n displays the text file starting at the sixth line. 
——————————————————————————————————————————————————————————————————
``` -j6 written_2/travel_guides/berlitz1/HandRIbiza.txt ```
``` 
        Recommended Hotels
        The establishments listed below offer a cross-section of
        local restaurants, and should convince you that not everything on the
        island comes with chips (french fries).
        The star rating in brackets after each entry refers to the
```
——————————————————————————————————————————————————————————————————
> setting -2 as the value for n displays the text file starting at the second last line. 
——————————————————————————————————————————————————————————————————
``` -j-2 written_2/travel_guides/berlitz1/HandRIbiza.txt ```
```     
        Recommended Hotels
        The establishments listed below offer a cross-section of
        local restaurants, and should convince you that not everything on the
        island comes with chips (french fries).
        The star rating in brackets after each entry refers to the
        offfical government rating system.
        As a basic guide, the symbols we use indicate what you can
        expect to pay for a three-course meal for two, excluding wine, tax and
        tip. Drinks will add considerably to the final bill.
        ✪less than 5,000 ptas. 
```
——————————————————————————————————————————————————————————————————

__-N or --LINE-NUMBERS__
> Dislplays line number at the beginning of each line. Useful in combination with other command options as well, like -jn.
——————————————————————————————————————————————————————————————————
> using -N to display the line numbers of a text file
——————————————————————————————————————————————————————————————————
``` less -N written_2/travel_guides/berlitz1/HandRHongKong.txt ```
``` 
      1 
      2   
      3   
      4     
      5         
      6         Recommended Hotels
      7         Hong Kong has some of the most luxurious hotels in the
      8         world, with representatives from all the major international chains.
      9         Hotels listed below have full air-conditioning, offer 24-hour or
     10         limited room service, and a wide range of facilities. Hong Kong hotels
     11         have excellent business services and conference facilities; many have
     12         shopping malls.
     13         Reservations are strongly recommended, particularly in
     14         summer and at Christmas. If you do arrive without making advance
     15         arrangements, the Hong Kong Hotel Reservation Center at the
     16         International Airport will be happy to arrange accommodations for you
     17         on your arrival.
     18         As a basic guide, the symbols below have been used to
     19         indicate high-season rates in Hong Kong dollars, based on double
     20         occupancy, with bath or shower. Unless otherwise noted, hotels take all
```
——————————————————————————————————————————————————————————————————
> using -N to display the line numbers of a text file in combination with the -jn option
——————————————————————————————————————————————————————————————————
``` less -N -j10 written_2/travel_guides/berlitz1/HandRHongKong.txt ```
``` 11         have excellent business services and conference facilities; many have
     12         shopping malls.
     13         Reservations are strongly recommended, particularly in
     14         summer and at Christmas. If you do arrive without making advance
     15         arrangements, the Hong Kong Hotel Reservation Center at the
     16         International Airport will be happy to arrange accommodations for you
     17         on your arrival.
     18         As a basic guide, the symbols below have been used to
     19         indicate high-season rates in Hong Kong dollars, based on double
     20         occupancy, with bath or shower. Unless otherwise noted, hotels take all
     21         major credit cards. A 10% service charge and 5% government tax will be
     22         added to the bill.
     23         $$$$above HK$2,500
     24         $$$HK$l,600 to HK$2,500
     25         $$HK$950 to HK$1,600
     26         $below HK$950
     
```
——————————————————————————————————————————————————————————————————

__-Blank__
> Explaination
——————————————————————————————————————————————————————————————————
> Example 1 
——————————————————————————————————————————————————————————————————
``` Input ```
``` Output ```
——————————————————————————————————————————————————————————————————
> Example 2
——————————————————————————————————————————————————————————————————
``` Input ```
``` Output ```
——————————————————————————————————————————————————————————————————

__-Blank__
> Explaination
——————————————————————————————————————————————————————————————————
> Example 1 
——————————————————————————————————————————————————————————————————
``` Input ```
``` Output ```
——————————————————————————————————————————————————————————————————
> Example 2
——————————————————————————————————————————————————————————————————
``` Input ```
``` Output ```
——————————————————————————————————————————————————————————————————

Sources:
``` https://man7.org/linux/man-pages/man1/less.1.html ```


Output Control:

The '-E' option will cause less to automatically exit when the end of the file is reached
The '-S' option will cause lines that are longer than the screen width to be truncated instead of wrapped

Other Features:
The 'v' command can be used to open a file in a text editor such as 'vi' for further editing
The 'q' key will quit less and return to the shell prompt
The 'h' key will display the help screen with a list of available commands.
These are just a few examples of the many features and subcommands available in the "less" command. By using the above subcommands and options, you can effectively navigate and manage text files in Linux.