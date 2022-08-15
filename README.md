from datetime import date

class Marvel:
    producer='kevin' #class variable
    ga=650 #in million
    no_of_movies=0
    
    def __init__(self, movie, hero, release ,director, budget):
        self.movie=movie
        self.hero=hero
        self.release=release
        self.director=director
        self.budget=budget
        Marvel.no_of_movies=Marvel.no_of_movies+1
        
    def label(self):
        lab=f"Movie : {self.movie}\nHero:{self.hero}\nrelease:{self.release}\ndirector:{self.director}\nbudget:{self.budget}"
        return lab
    def no_of_year_after_release(self):
        current_year=date.today().year
        no_of_year=current_year-self.release
        return no_of_year
    
    def gain (self, collection):
        self.ga=collection-self.budget
        
movie1=Marvel('iron man', 'tony', 2008, 'jon', 140)
movie2=Marvel('the incredible hulk' ,'hulk' , 2008, 'louis', 150)
movie2.producer='gale'
movie1.gain(585)
print(movie2.label())
print(movie1.label())
print(movie1.no_of_year_after_release())
print(movie2.producer)
print(movie1.producer)  
print(movie2.ga)
print(movie1.ga)
print(Marvel.no_of_movies)
