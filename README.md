Honestly, the code has been written in a good way, OOP Usage on MC from MVC pattern for the application data and business logic. there are things that can improve according to me.

Classes/Function are not based on Single Responsibility of (SOLID) principle. which need to be broken into different Traits/Interfaces for neat and clean code and re-usability.

Some function contains too many if/else if statement making it harder to trace logic. There are even several ifs that can be combined.

Setting default values for variable and array['key'] values was done a lot. It would be nice to have a helper method just to set the default value for each of them instead of writing the same statement over and over.

I think it would be nice to have a Wrapper Model called 'BookingRequest', or 'JobRequest', or maybe use the Job Model and store all the validations and behaviors in there so that the BookingRepository@store method would be cleaner.

SMS notifications and Pushrs could be in another Wrapper Model so that they could be easily reused for other Repositories.

Some variables are declared and initialized in the middle of a code block. They must be written at the beginning of a code block.

I think it's better to use guzzlehttp/guzzle for reaching out to external API

Localization/Language-file are not used.

convertToHoursMins- this function should be part of the Helper class which can be used globally in the project.