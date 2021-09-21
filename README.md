# Cpp_ConcurrentTrafficSimulation_L2
This is a training for writing a concurrent program in C++

This is the second lesson's excercise. The code explanation is provided by Prof. Andreas Haja in the Youtube links below:
https://www.youtube.com/watch?v=hYQus_Yieu4&t=675s&ab_channel=Udacity \
https://www.youtube.com/watch?v=1rcgMOF996k&ab_channel=Udacity

## The Project's Description:

### Project Tasks
**Task L2.1 :** In method Vehicle::drive(), start up a task using std::async which takes a reference to the method Intersection::addVehicleToQueue, the object _currDestination and a shared pointer to this using the get_shared_this() function. Then, wait for the data to be available before proceeding to slow down. \
*The following links are useful for this task:* \
https://stackoverflow.com/questions/11758414/class-and-stdasync-on-class-member-in-c \
https://www.reddit.com/r/learnprogramming/comments/2gavlf/c11_what_is_the_proper_way_to_pass_a_member/

**Task L2.2 :** In method Intersection::addVehicleToQueue(), add the new vehicle to the waiting line by creating a promise, a corresponding future and then adding both to _waitingVehicles. Then wait until the vehicle has been granted entry.\

**Task L2.3 :** In method WaitingVehicles::permitEntryToFirstInQueue(), get the entries from the front of _promises and _vehicles. Then, fulfill promise and send signal back that permission to enter has been granted. Finally, remove the front elements from both queues. \
*The following links are useful for this task:* \
https://stackoverflow.com/questions/40656871/remove-from-the-beginning-of-stdvector

You can find these tasks in the project_tasks.txt within the workspace as well.

### Build Instructions
To compile and run the code, create a build directory and use cmake and make as follows:
../L1_Project# mkdir build \
../L1_Project# cd build \
../L1_Project/build# cmake .. \
../L1_Project/build# make \
../L1_Project/build# ./traffic_simulation
