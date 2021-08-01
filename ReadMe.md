Corpus-based Synonym Finder  Author:   B a n k o l e   M o s e s   

 W H A T   T H E   CODE DOES:     T h e  Corpus-based Synonym Finder
i l l u s t r a t e s   a   p r i n c i p l e   o f   N a t u r a l 
 L a n g u a g e   P r o c e s s i n g ,   i t   s h o w s   t h a t 
 a   c o m p u t e r   c a n   e s t i m a t e   t h e   m e a n i n g 
 o f   w o r d s   i n   a   l a n g u a g e   w i t h o u t   a n 
 i n h e r e n t   u n d e r s t a n d i n g   o f   t h a t 
 l a n g u a g e .   

T h e   l a n g u a g e   u s e d   f o r   t h i s   p r o j e c t 
 w a s   Y o r u b a   b u t   t h e   c o d e   s u p p o r t s 
 a n y   l a n g u a g e   a t   a l l   a s   l o n g   a s   two
conditions are met

    1. Th e   c h a r a c t e r s   o f   t h e   l a n g u a g e   e x i s t s   i n   p y t h o n 's   c h a r a c t e r   m a p .
    2. The l a n g u a g e  uses . (dot / full stop) to denote the end of a sentence.

   H O W   T O   R U N   T H E   C O D E   :     T h e 
 s y n o n y m * f i n d e r . p y   i s   t h e   p y t h o n 
 f i l e   t h a t   s h o u l d   b e   r u n   w h e n 
 t e s t i n g   t h e   c o d e .   F o r   t h e   c o d e   t o 
 r u n   e n s u r e   t h a t   t h e 
 Y o r u b a * c o r p u s . t x t   a n d 
 s e n t e n c e * t o k e n i z e r . p y   are   i n   t h e 
 s a m e   f o l d e r   a s   t h e 
 s y n o n y m * f i n d e r . p y 

 To change the Corpus-based Synonym Finder's language: 1. Move a corpus
text file of the language of choice into the Synonym Finder Folder 2.
Feed the corpus_words_txt (line 235) variable the name of the corpus
(must include .txt) 3. Note that the larger the corpus word count,
t h e   higher the a c c u r a c y   a n d  the slower the  s p e e d 
 o f   e x e c u t i o n 

 H O W   T H E   C O D E   W O R K S ( S I M P L I F I E D ) :   
 T h e   c o d e   w o r k s   b y   s e a r c h i n g   f o r   h o w 
 t h e   t a r g e t   w o r d   i s   u s e d   i n   a 
 s e n t e n c e   a n d   u s i n g   t h a t   k n o w l e d g e 
 t o   f i n d   o t h e r   w o r d s   ( s y n o n y m s )   t h a t 
 w e r e   u s e d   i n   s i m i l a r   c o n t e x t ,   s o 
 t h e   a c c u r a c y   a n d   s p e e d   o f   e x e c u t i o n 
 o f   t h e   s y n o n y m   f i n d e r   c o d e   i s 
 d e p e n d e n t   o n   t h e   s i z e   o f   t h e 
 c o r p u s .     

The Corpus-based Synonym Finder finds word synonyms by using the
position of the target words to find similar words by searching for
words used in similar contexts (positions).

The create_sentence_list function splits the whole corpus into
sentences ,it is computationally expensive especially for very large
corpus. Using a database to index the sentences in a corpus means the
function only has to run once and it could speed up code execution.

Note: In the synonym_word_list, the more a word appears, the higher
probability of the word being a synonym
