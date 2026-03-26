## 1. Image / Video Dataset (Core Requirement)

Used for training **CNN (object detection)**

![[data4.jpeg]]

![[data3.jpeg]]

![[data2.jpeg]]

![[data.jpeg]]
### What it should contain:
- Animals on tracks (cow, elephant, dog, etc.)
- Humans near/on tracks
- Objects (rocks, debris, vehicles)
- Different conditions:
    - Day / Night
    - Rain / Fog
    - Different angles

### Format:
- Images or video frames
- Annotated with bounding boxes + labels

**Example labels:**
- `animal`
- `human`
- `obstacle`
## 2. Time-Series Dataset (For LSTM)

Used for **prediction (movement & collision timing)**
### What it should contain:
- Object position over time (frame-by-frame)
- Speed of object
- Direction of movement
- Distance from track
### Example:

|Time|Object|X, Y Position|Speed|
|---|---|---|---|
|t1|Cow|(120, 300)|2 m/s|
|t2|Cow|(140, 310)|2.2 m/s|

## 3. Distance & Train Data (Critical for Safety)

Used for **collision prediction logic**
### Required data:
- Train speed
- Braking distance
- Track curvature
- Sensor/camera position
### Purpose:
- Calculate:
    - Distance to object
    - Time to collision
    - Safe stopping time
## 4. Sensor Dataset 

If using IoT sensors:
### Includes:
- Motion sensors
- Vibration sensors
- Infrared (IR) detection
### Use:
- Improve detection accuracy
- Backup when vision fails (fog/night)
## 5. Annotation Requirements (Very Important)

Your dataset must be **labeled**:
- Bounding boxes around objects
- Class labels (animal/human/object)
- Optional:
    - Distance label
    - Movement direction

**Tool:**
- LabelImg