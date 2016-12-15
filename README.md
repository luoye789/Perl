# Perl
程序员编写的程序叫做源代码，简称为源/代码。模块就是Perl代码的集合。
常用模块：
        1）随机选取数组的一个元素：
        #!/usr/bin/perl -w
        use strict;
        use warnings;
        #声明变量
        my $count;
        my $input;
        my $sentence;
        my $story;
        my @nouns = ('Dad', 'TV', 'Mom', 'Rebecca', Joe and Moe',);
        my @verbs = ('ran to', 'giggled with', 'jumped with', dissolved', 'sang stupid songs with',);
        my @preposition = ('at the store', over the rainbow', 'just for the fun of it', 'in a dream', in New York City',);
        #随机选取数组的一个元素
        srand( time | $$ ); #time：进程ID；  |：位或；  $$：设置随机化种子（指定种子，固定的种子每次得到的结果一样）
        do {
        $story = '';       #清空一个字符串
        for ( $count = 0 ;$count < 6 ; $count++ )  {
        $sentence =
            $nouns[ int( rand( scalar @nouns ) ) ] . " "                    #函数scalar返回数组元素的个数 $verbs[ int( rand(7))]
           .$verbs[ int( rand( scalar @verbs ) ) ] . " "                    #rand(7)返回一个大于0，小于7的（伪）随机数，这是一个浮点数。
           .$nouns[ int( rand( scalar @nouns ) ) ] . " "                    #$verbs[int(3.47429)]，[int(3.47429)]仅返回它的整数部分。
           .$preposition[ int( rand( scalar @preposition ) ) ] . '. ';      #$verbs(3)则返回数组nouns的第四个元素。
           $story .= $sentence;                                             $story .= =$story.$sentence
          }
          print "\n", $story, "\n" ;
          print "\nTepy \"quit\" to quit,or press Enter to continue: ";
          $input = <STDIN>;
        }until ( $input =~ /^\s*q/i );
        exit;
        
        2)在字符串中选取一个随机位置
          
        3)生成随机DNA（长度不一，每个位置上的碱基种类可能不同
        
        
        
