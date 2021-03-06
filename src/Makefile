CC = gcc            # default is CC = cc
CFLAGS = -g -Wall   # default is CFLAGS = [blank]
AR = ar -cvq
RANLIB = ranlib
PROJ_DIR = ..
INC_DIR = $(PROJ_DIR)/include
LIB_DIR = $(PROJ_DIR)/lib
TEST_DIR = $(PROJ_DIR)/test
GTTHREADS_SRC = gtthread_sched.c gtthread_mutex.c steque.c
GTTHREADS_OBJ = $(patsubst %.c,%.o,$(GTTHREADS_SRC))
HEADER = gtthread.h steque.h
LIBRARY = libgtthread.a

# pattern rule for object files
%.o: %.c
	$(CC) -c $(CFLAGS) $< -o $@

all: $(GTTHREADS_OBJ) library

library: $(GTTHREADS_OBJ)
	$(AR) $(LIB_DIR)/$(LIBRARY) $(GTTHREADS_OBJ)
	$(RANLIB) $(LIB_DIR)/$(LIBRARY)
	cp -f $(HEADER) $(INC_DIR)   

copy:
	cp -f $(HEADER) $(INC_DIR)  

test1: $(GTTHREADS_OBJ)
	$(CC) -o $(TEST_DIR)/test1/main -I$(INC_DIR) $(GTTHREADS_OBJ) $(TEST_DIR)/test1/main.c 
	./$(TEST_DIR)/test1/main 

test2: $(GTTHREADS_OBJ)
	$(CC) -o $(TEST_DIR)/test2/main -I$(INC_DIR) $(GTTHREADS_OBJ) $(TEST_DIR)/test2/main.c 
	./$(TEST_DIR)/test2/main  

test3: $(GTTHREADS_OBJ)
	$(CC) -o $(TEST_DIR)/test3/main -I$(INC_DIR) $(GTTHREADS_OBJ) $(TEST_DIR)/test3/main.c 
	./$(TEST_DIR)/test3/main   

test4: $(GTTHREADS_OBJ)
	$(CC) -o $(TEST_DIR)/test4/main -I$(INC_DIR) $(GTTHREADS_OBJ) $(TEST_DIR)/test4/main.c 
	./$(TEST_DIR)/test4/main    

test5: $(GTTHREADS_OBJ)
	$(CC) -o $(TEST_DIR)/test5/main -I$(INC_DIR) $(GTTHREADS_OBJ) $(TEST_DIR)/test5/main.c 
	./$(TEST_DIR)/test5/main     

test6: $(GTTHREADS_OBJ)
	$(CC) -o $(TEST_DIR)/test6/main -I$(INC_DIR) $(GTTHREADS_OBJ) $(TEST_DIR)/test6/main.c 
	./$(TEST_DIR)/test6/main      

test7: $(GTTHREADS_OBJ)
	$(CC) -o $(TEST_DIR)/test7/main -I$(INC_DIR) $(GTTHREADS_OBJ) $(TEST_DIR)/test7/main.c 
	./$(TEST_DIR)/test7/main       

test8: $(GTTHREADS_OBJ)
	$(CC) -o $(TEST_DIR)/test8/main -I$(INC_DIR) $(GTTHREADS_OBJ) $(TEST_DIR)/test8/main.c 
	./$(TEST_DIR)/test8/main        

test9: $(GTTHREADS_OBJ)
	$(CC) -o $(TEST_DIR)/test9/main -I$(INC_DIR) $(GTTHREADS_OBJ) $(TEST_DIR)/test9/main.c 
	./$(TEST_DIR)/test9/main         

test10: $(GTTHREADS_OBJ)
	$(CC) -o $(TEST_DIR)/test10/main -I$(INC_DIR) $(GTTHREADS_OBJ) $(TEST_DIR)/test10/main.c 
	./$(TEST_DIR)/test10/main          

test11: $(GTTHREADS_OBJ)
	$(CC) -o $(TEST_DIR)/test11/main -I$(INC_DIR) $(GTTHREADS_OBJ) $(TEST_DIR)/test11/main.c 
	./$(TEST_DIR)/test11/main           

test12: $(GTTHREADS_OBJ)
	$(CC) -o $(TEST_DIR)/test12/main -I$(INC_DIR) $(GTTHREADS_OBJ) $(TEST_DIR)/test12/main.c 
	./$(TEST_DIR)/test12/main             

testall: test1 test2 test3 test4 test5 test6 test7 test8 test9 test10 test11

clean:
	$(RM) -f *.o $(LIB_DIR)/* $(GTTHREAD_OBJ)
