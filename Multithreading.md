# Multithreading
```
...
#include <pthread.h>
void *laufenlassen(void *tid){
	long id = (long) id
	std::cout << “working hard at “ << *tid << std::endl;
	pthread_exit(NULL);
}

int main(int argc, char const *argv[]){
	pthread_t arr[10];
	pthread_attr_t attribute;
	pthread_atrr_init(&attribute);
	pthread_attr_setdetachstate(&attribute, PTHREAD_CREATE_JOINABLE);
	for (long i = 0; i < 10; i++){
		std::cout << “Creating thread “ << i << std::endl;
		pthread_create(&arr[i], &attribute, laufenlassen, (void *)i);
		pthread_join(arr[i], &status)
	}
	void *status;
	for (long i = 0; i < 10; i++){
		pthread_join(arr[i], &status);
		std::cout << “Thread ” << i << “ ist fertig.” << std::endl;
	return 0;
}
```
Zum Kompilieren: g++ datei.cpp -lpthread
