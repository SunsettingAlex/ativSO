import time
import threading
from threading import Semaphore

numero = 0
mutex = Semaphore(1)

def p1():
    global numero
    while True:
        global mutex
        mutex.acquire() #down (adiquire)
        numero += 1
        print('P1:', numero)
        mutex.release() #up (libera)
        time.sleep(1)

def p2():
    global numero
    while True:
        global mutex
        mutex.acquire() # down
        numero += 1
        print('P2:', numero)
        mutex.release() # up
        time.sleep(1)


t_p1 = threading.Thread(target=p1)
t_p2 = threading.Thread(target=p2)

print('Alex Loureiro Soares')
t_p1.start()
t_p2.start()
