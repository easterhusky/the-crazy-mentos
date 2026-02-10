import numpy as np
import matplotlib.pyplot as plt


T0 = 200        
T_room = 25    
k = 0.1        
t_end = 20     


t = np.linspace(0, t_end, 100)


T = T_room + (T0 - T_room) * np.exp(-k * t)


T_20 = T_room + (T0 - T_room) * np.exp(-k * t_end)
print("temperature after 20 minutes:", round(T_20, 2), "°C")


plt.figure()
plt.plot(t, T)
plt.xlabel("time (minutes)")
plt.ylabel("temperature (°C)")
plt.title("engine cooling after shutdown")
plt.grid(True)
plt.show()
