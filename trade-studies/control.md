# RC Car Landspeed World Record – Trade Study (UK)  
**Scope:** controller interface (human controls), transmitter + receiver (control link), and telemetry (downlink).  
**Range targets:** “cheap & good enough” (few hundred m), and **long-range up to ~5 km** (clear line-of-sight, correct antennas, and testing required).

---

## Quick picks (if you just want a short list)

### If you genuinely need ~5 km reliability
**Most “plug-and-go proven” path:** **TBS Crossfire (868)**  
- **Gamepad TX:** **TBS Tango 2** (Crossfire built in) – **£159.90, in stock** :contentReference[oaicite:0]{index=0}  
- **RX:** **TBS Crossfire Nano RX (SE)** – **~£29.90, in stock** :contentReference[oaicite:1]{index=1}  
- **Why:** UHF 868 penetrates better and holds link margin far beyond typical 2.4 GHz surface radios.

### If you want cheap short/mid-range (and simple)
- **FlySky GT5 + BS6 RX** – **£102.99** (UK retailer) :contentReference[oaicite:2]{index=2}  
- **RadioLink RC6GS V3 + R7FG** – **£99.74, in stock** :contentReference[oaicite:3]{index=3}  
- **DumboRC X6PM set** – **£34.99 (listed), but sold out at that listing** :contentReference[oaicite:4]{index=4}  

---

# 1) Controller interface trade study (how you drive it)

## A) Pistol-grip “surface” radios (most intuitive at high speed)
**Pros**
- Best for steering precision + throttle modulation at extreme speed.
- Ergonomics are designed for cars.

**Cons**
- Most are **2.4 GHz** and not designed for multi-km out of the box.

**Notable options (UK pricing / availability):**
- **RadioMaster MT12 (surface, EdgeTX)** – **£129.99, in stock** :contentReference[oaicite:5]{index=5}  
  - Big deal: it’s open + has a module bay that can take long-range modules (e.g., Crossfire Nano module class). :contentReference[oaicite:6]{index=6}  
- **Futaba T4PM Plus (with RX)** – **£242.99, in stock** :contentReference[oaicite:7]{index=7}  
- **Sanwa MT-5 (with RX)** – **£260.99** :contentReference[oaicite:8]{index=8}  
- **RadioLink RC8X kit** – **£365.74** :contentReference[oaicite:9]{index=9}  
- **FlySky Noble NB4 Pro+ (premium wheel radio)** – **£429.00, in stock** :contentReference[oaicite:10]{index=10}  
  - Note: product page claims “>300 m (open ground)” for that system. :contentReference[oaicite:11]{index=11}  

## B) Gamepad-style controllers (compact, easy to hold steady)
**Pros**
- Comfortable for long runs, easy to brace on a tripod/stand.
- Great pairing with long-range FPV-style links.

**Cons**
- Less “car native” than a wheel for some drivers.

**Options**
- **TBS Tango 2 (Crossfire inside)** – **£159.90, in stock** :contentReference[oaicite:12]{index=12}  

## C) Stick radios (aircraft style) – surprisingly strong for long-range
**Pros**
- Massive ecosystem (EdgeTX/OpenTX), easy to add long-range modules, logging, custom switches.
- Best if you’ll later add autopilot/“flight controller”-like logic.

**Cons**
- Steering on a stick can be harder at very high speed unless you practice.

**Options**
- **RadioMaster Boxer (ELRS)** – **£139.99, in stock** :contentReference[oaicite:13]{index=13}  
- **RadioMaster TX16S MKII (4in1)** – **£180.00, in stock** :contentReference[oaicite:14]{index=14}  

---

# 2) Transmitter + receiver (CONTROL LINK) trade study

## Range reality check (simple rule)
- **2.4 GHz surface radios:** usually “plenty” for normal RC, but **multi-km is not what most are designed for**.
- **868 MHz UHF (UK):** the common choice when you truly need km-class reliability.

---

## A) Cheaper short-range (best value; likely fine if you’re not actually multi-km)
These are “cheap and cheerful” picks if your actual operator position stays close to the run (or you can follow the car).

### 1) DumboRC (very budget)
- **TX+RX set:** **£34.99 (listed)** (example listing shows sold out) :contentReference[oaicite:15]{index=15}  
**Benefits:** extremely low cost, quick to get running.  
**Drawbacks:** not the link you choose for a record attempt where failsafe margin matters.

### 2) FlySky GT5 (budget, popular)
- **TX+RX:** **£102.99** :contentReference[oaicite:16]{index=16}  
**Benefits:** solid budget feature set, common ecosystem.  
**Drawbacks:** still fundamentally a typical 2.4 GHz surface link (test range carefully).

### 3) RadioLink RC6GS V3 (value + telemetry/gyro receiver)
- **TX+RX:** **£99.74, in stock** :contentReference[oaicite:17]{index=17}  
- Page lists “ground distance up to 600 m.” :contentReference[oaicite:18]{index=18}  
**Benefits:** good feature/price, telemetry support, respectable spec.  
**Drawbacks:** “600 m” class is not “5 km class”.

---

## B) Higher-end 2.4 GHz surface radios (excellent feel; still not “true 5 km”)
### 1) Futaba T4PM Plus
- **£242.99, in stock** :contentReference[oaicite:19]{index=19}  
**Benefits:** top-tier control feel, reliability, racing pedigree.  
**Drawbacks:** still 2.4 GHz; don’t assume multi-km without testing.

### 2) Sanwa MT-5
- **£260.99** :contentReference[oaicite:20]{index=20}  
**Benefits:** very strong performance/latency reputation in racing circles.  
**Drawbacks:** same “2.4 GHz range ceiling” concern.

### 3) RadioLink RC8X
- **£365.74** :contentReference[oaicite:21]{index=21}  
**Benefits:** very feature-rich; page states “600 m range.” :contentReference[oaicite:22]{index=22}  
**Drawbacks:** pricey for a “not truly multi-km” class system.

### 4) FlySky Noble NB4 Pro+
- **£429.00, in stock** :contentReference[oaicite:23]{index=23}  
**Benefits:** premium ergonomics + features.  
**Drawbacks:** page itself quotes **>300 m open ground**, so you should not treat it as a km-class system. :contentReference[oaicite:24]{index=24}  

---

## C) Long-range (up to ~5 km) – the “record attempt” category

### Option C1) **TBS Crossfire (868 MHz) – most straightforward**
**Transmitter-side choices**
- **TBS Tango 2 (Crossfire built in):** **£159.90, in stock** :contentReference[oaicite:25]{index=25}  
- **Crossfire Micro TX V2 module:** **£74.90 (listing shows out of stock)** :contentReference[oaicite:26]{index=26}  
- **Crossfire full-size module:** **£214.90 (listing shows out of stock)** :contentReference[oaicite:27]{index=27}  
- **Micro TX V2 Starter Set (module + 3 receivers):** **£119.90, only 2 left** :contentReference[oaicite:28]{index=28}  

**Receiver choices**
- **Crossfire Nano RX (SE):** **£29.90, in stock** :contentReference[oaicite:29]{index=29}  

**Benefits**
- Designed for long range; strong ecosystem; commonly used for km-class control links.
- Works well with directional antennas and elevated ground station setups.

**Drawbacks**
- More expensive than budget 2.4 GHz.
- You must configure failsafe and thoroughly validate before high-speed runs.

---

### Option C2) **ExpressLRS 868 MHz (ELRS) – potentially cheaper, BUT UK compliance is tricky**
**TX module example**
- **Bandit 915/868 RF Module:** **£99.50, only 2 left** :contentReference[oaicite:30]{index=30}  
  - That same listing warns it’s **not UK legal** (no LBT firmware per that seller’s note). :contentReference[oaicite:31]{index=31}  

**Receiver examples**
- **RadioMaster Bandit BR1 868 RX:** **£19.99, in stock** :contentReference[oaicite:32]{index=32}  
- **Sequre 915/868 True Diversity RX:** **£22.00** :contentReference[oaicite:33]{index=33}  
- **Happymodel ES900 Dual Diversity 868 RX:** **£17.59** :contentReference[oaicite:34]{index=34}  

**Benefits**
- Very low receiver cost; lots of hardware choices.
- Great performance *when configured legally and correctly*.

**Drawbacks (important)**
- UK rules + LBT/regional settings matter; sellers explicitly warn about legality depending on firmware/band. :contentReference[oaicite:35]{index=35}  
- If you want the “least regulatory headache,” Crossfire is usually simpler in practice.

---

## D) “Best-of-both” hybrid approach (common for record projects)
**Idea:** Use a **very robust long-range control link** (Crossfire/868), and handle **telemetry separately** (either on the same link, or via a dedicated modem).

**Why do this?**
- Control stays rock solid; telemetry can be tuned/expanded without risking steering/throttle.

---

# 3) Telemetry (DOWNLINK) options (UK)

## A) Use telemetry built into the control system (simplest)
**Pros**
- One radio link to manage.
- Enough for “link health + battery + basic sensors” if your RX/FC supports it.

**Cons**
- Telemetry bandwidth is limited; adding lots of sensors/logging can be painful.

(Example: some systems like RadioLink RC6GS advertise telemetry features. :contentReference[oaicite:36]{index=36})

## B) Dedicated long-range telemetry modem (separate “data pipe”)
**Option:** **RFD868x v2 (868 MHz telemetry modem)**
- Example bundle listing: **£280.00** :contentReference[oaicite:37]{index=37}  
- Another UK listing shows **£120.83** (single modem) :contentReference[oaicite:38]{index=38}  
- Another listing shows **£97.53** (out of stock) :contentReference[oaicite:39]{index=39}  

**How it’s used (simple):**
- You typically need **two units** (ground + vehicle), plus antennas.
- Run telemetry (speed, battery, temps, GPS if used) through this link.

**Pros**
- Can be extremely robust for telemetry, independent of the control link.
- Easier to scale telemetry features.

**Cons**
- Extra cost, wiring, antennas, integration work.

---

# 4) Receiver integration notes (because your “flight controller” is unknown)

You’ll likely face one of these:
1) **Direct PWM** to ESC + steering servo (simplest)
2) Serial protocol (**CRSF**, etc.) into a controller/autopilot, which then outputs to ESC/servo

**Practical advice**
- If you don’t know the controller yet, pick an RX path that can still do **PWM output today** (so you can drive ESC/servo immediately).
- Crossfire Nano RX is often used with CRSF; many users pair it with a controller that understands CRSF. (If you want PWM-only, you’ll plan for a CRSF→PWM solution or a receiver that provides PWM outputs.)

---

# 5) Simple decision guide (choose based on your real range)

## If your operator can stay within ~0.5–1 km of the car
Pick a good 2.4 GHz surface system:
- **RadioLink RC6GS V3** (~£99.74) :contentReference[oaicite:40]{index=40}  
- **FlySky GT5** (~£102.99) :contentReference[oaicite:41]{index=41}  
- **Futaba / Sanwa** if you want premium feel :contentReference[oaicite:42]{index=42}  

## If you want “5 km class” margin
Pick 868 control:
- **TBS Tango 2 + Crossfire Nano RX** :contentReference[oaicite:43]{index=43}  
or  
- **Surface wheel feel + long-range:** **RadioMaster MT12** + long-range module capability :contentReference[oaicite:44]{index=44}  

## If you want maximum instrumentation
- **Crossfire (control)** + **RFD868x (telemetry)** :contentReference[oaicite:45]{index=45}  

---

## If you want, I can also output this as:
- a “shopping list” (3 builds: budget / mid / record-grade),
- and a one-page test plan (range test, failsafe validation, antenna placement checklist).
