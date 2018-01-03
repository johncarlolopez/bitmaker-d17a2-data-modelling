1.
  * Actor
    * id(integer)
    * name(string)
  * Role
    * id(integer)
    * name(string)
  * Play
    * id(integer)
    * name(string)
    * director_id(integer)(foreign key)
  * Cast
    * id(integer)
    * actor_id(string)(foreign key)
    * role_id(string)(foreign key)
    * play_id(string)(foreign key)
  * Director
    * id(integer)
    * name(string)

Actor(one) - (many)Role
Role(many) - (many)Play
Role(one) - (many) Cast (many) - (one) Play
Play(many) - (one)Director

2.
  * Breed
    * id(integer)
    * name(string)
  * Pet
    * id(integer)
    * name(string)
    * breed_id(integer)(foreign key)
    * owner_id(integer)(foreign key)
  * Veterinarian appointment
    * id(integer)
    * pet_id(integer)(foreign key)
    * vet_id(integer)(foreign key)
    * clinic_id(integer)(foreign key)
    * time(string)
  * Veterinarian
    * id(integer)
    * name(string)
    * clinic_id(integer)(foreign key)
  * Animal clinic
    * id(integer)
    * name(string)
  * Pet owner
    * id(integer)
    * name(string)

Pet (one) - (one) Breed
Pet (one) - (many) vet appointments
Vet appointment (many) - (one) vet
vet (many) - (one) animal clinic
vet appointment (many) - (one) animal clinic
pet (many) - (one) pet owner

3.
  * Restaurant
    * id(integer)
    * name(string)
  * Review
    * id(integer)
    * name(string)
    * restaurant_id(integer)(foreign key)
    * food_critic_id(integer)(foreign key)
  * Food critic
    * id(integer)
    * name(string)
    * publication_id(integer)(foreign key)
  * Publication
    * id(integer)
    * name(string)
  * Chef
    * id(integer)
    * name(string)
    * restaurant_id(integer)(foreign key)

restaurant (one) - (many) reviews
restaurant (one) - (many) chefs
food critic (one) - (many) reviews
publication (one) - (many) food critics


Ask an instructor to look over your answers before moving on to Part 3 to make sure you're on the right track.*
