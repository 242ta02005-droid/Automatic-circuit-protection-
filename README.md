# Automatic-circuit-protection-
# Automatic Circuit Protection System

MIN_VOLTAGE = 200
MAX_VOLTAGE = 250
MAX_CURRENT = 10
MAX_TEMPERATURE = 70

print("==============================")
print("   AUTOMATIC CIRCUIT PROTECTION")
print("==============================")

voltage = float(input("Enter voltage (V): "))
current = float(input("Enter current (A): "))
temperature = float(input("Enter temperature (°C): "))

fault = False

# Voltage protection
if voltage < MIN_VOLTAGE:
    print("⚠️ Under-voltage detected")
    fault = True

elif voltage > MAX_VOLTAGE:
    print("⚠️ Over-voltage detected")
    fault = True

# Current protection
if current > MAX_CURRENT:
    print("⚠️ Overcurrent detected")
    fault = True

# Temperature protection
if temperature > MAX_TEMPERATURE:
    print("⚠️ Overheating detected")
    fault = True

# Automatic protection
if fault:
    print("\n🔴 FAULT DETECTED")
    print("⚡ Automatic Protection ACTIVATED")
    print("🔌 Circuit DISCONNECTED")

else:
    print("\n🟢 CIRCUIT NORMAL")
    print("✅ Protection System: READY")
    print("⚡ Circuit remains CONNECTED")
