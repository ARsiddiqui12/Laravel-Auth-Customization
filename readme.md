Laravel Auth Customization 

Login with Employee Id and password 

Step1: Configure Database Details in "ENV" file 

Step2: Open Command Prompt on specific folder and write this statement " PHP artisan migrate:refresh "

Step3: Register a new Employee with all details

step4: Run the project and login with Employee ID

--------------------------------------------------------------------------------------------------------------------------

Migration Table Structure

Schema::create('users', function (Blueprint $table) {
            $table->increments('id');
            $table->string('username')->unique();
            $table->string('employeeid')->unique();
            $table->string('cnicnumber')->unique();
            $table->string('email')->unique();
            $table->string('password');
            $table->rememberToken();
            $table->timestamps();
        });
