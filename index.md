__Less Command in Linux__
> The "less" command in Linux is a powerful utility used for viewing and navigating through text files. It is often used as an alternative to the "more" command and offers additional features such as the ability to move both forwards and backwards within the file, search for text, and perform other advanced operations.


__Command Line Options__ 
> -jn or --jump-target=n

> -n or --line-numbers

> -bn or --buffers=n

> -Dxcolor or --color=xcolor

__-jn or --jump-target=n__
> The -j command option allows you to jump to a specific target line as specified by the variable 'n' in the command. The number specified starts from the first line at 1, but can also be used to jump from the back by using negative numbers as inputs, with -1 being the last line. Additionally, decimal numbers can be used to travel a perentage of the screen down, with .3 being 30% down and .5 being half down.

> setting 8 as the value for n displays the text file starting at the sixth line. 

>``` less -j6 written_2/travel_guides/berlitz1/HandRIbiza.txt ```
``` 
        Recommended Hotels
        The establishments listed below offer a cross-section of
        local restaurants, and should convince you that not everything on the
        island comes with chips (french fries).
        The star rating in brackets after each entry refers to the
```

> setting -2 as the value for n displays the text file starting at the second last line. 

>``` less -j-2 written_2/travel_guides/berlitz1/HandRIbiza.txt ```
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


__-N or --LINE-NUMBERS__
> Dislplays line number at the beginning of each line. Useful in combination with other command options as well, like -jn.

> using -N to display the line numbers of a text file

>``` less -N written_2/travel_guides/berlitz1/HandRHongKong.txt ```
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

> using -N to display the line numbers of a text file in combination with the -jn option

>``` less -N -j10 written_2/travel_guides/berlitz1/HandRHongKong.txt ```
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


__-bn or --buffers=n__
> allows users to specify how much buffer space to allocate for use with each file, where n is a value in kilobytes. This is useful to reduce the amount of workload put on the machine to look through larger files. If n is set to -1, the buffer space is unlimited. The examples below can't explain the difference in behaviour becuase it is change in timing, but are there none the less.

> buffer space is set to 160

>``` less -b160 written_2/travel_guides/berlitz1/HandRHawaii.txt ```
``` 
        Oahu (Including Honolulu)
        Aston Waikiki Sunset $$$ 229 Paoakalani Avenue, Honolulu, HI
        96815; Tel. (808) 922-2700 or (800) 336-5599; fax (808) 922-8785;
        <www.aston-hotels.com>. One of Aston’s many condominium resort
        properties, this modern high-rise has large rooms with complete 
```

> buffer space is set to -1

>``` less -b-1 written_2/travel_guides/berlitz1/HandRHawaii.txt ```
``` 
        Oahu (Including Honolulu)
        Aston Waikiki Sunset $$$ 229 Paoakalani Avenue, Honolulu, HI
        96815; Tel. (808) 922-2700 or (800) 336-5599; fax (808) 922-8785;
        <www.aston-hotels.com>. One of Aston’s many condominium resort
        properties, this modern high-rise has large rooms with complete 
```


__-Dxcolor or --color=xcolor__
> Sets the color of a specifced part of the text to a given color value. This can be useful for organzing data files according to different specifcations. The options are as follows: 
``` 
  B      Binary characters.
  C      Control characters.
  E      Errors and informational messages.
  H      Header lines and columns, set via the --header option.
  M      Mark letters in the status column.
  N      Line numbers enabled via the -N option.
  P      Prompts.
  R      The rscroll character.
  S      Search results.
  W      The highlight enabled via the -w option.
  d      Bold text.
  k      Blinking text.
  s      Standout text.
```
>
> 'x' a character sets the type of text whose color is being changed 
> 'color' is either a 4-bit color string or an 8-bit color string:

> using the N option with the -n option to display colored line numbers for the following text file.

>``` less -N -j10 --color=Nblue written_2/travel_guides/berlitz1/HandRHongKong.txt ```

``` 
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
     21         major credit cards. A 10% service charge and 5% government tax will be
     22         added to the bill.
     23         $$$$above HK$2,500
     24         $$$HK$l,600 to HK$2,500
     25         $$HK$950 to HK$1,600
     26         $below HK$950
     
```

> using the tag B and the color red to display binary numbers in red for the following text file. 

>``` less --color=Bred written_2/travel_guides/berlitz1/HandRHawaii.txt ```
``` 
        Oahu (Including Honolulu)
        Aston Waikiki Sunset $$$ 229 Paoakalani Avenue, Honolulu, HI
        96815; Tel. (808) 922-2700 or (800) 336-5599; fax (808) 922-8785;
        <www.aston-hotels.com>. One of Aston’s many condominium resort
        properties, this modern high-rise has large rooms with complete 
```


>Sources:
>``` https://man7.org/linux/man-pages/man1/less.1.html ```
