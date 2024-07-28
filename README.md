# Face-Recognition-with-voice
## Tutorial Requirements
- Python version 3.8.10
- A webcam (your laptop’s built-in webcam or an external one)

## Step 0: Clone repo and install dependencies
Clone this example project, and change into the directory from the command line.

     git clone https://github.com/UdaySMukherjee/Face-Recognition-with-voice.git
     cd facial-recognition

Create a virtual environment called `venv`. Activate the virtual environment, and then install the required Python packages inside the virtual environment. If you’re on Unix or Mac operating systems, enter these commands in a terminal.

    python3 -m venv venv
    source venv/bin/activate
    pip install -r requirements.txt

## Step 1: Create a custom face recognition dataset
Create a new subfolder inside the `dataset` directory using your first name, like `Uday`, to contain your photos.

    python3 headshots.py Uday

Then run this command to open a new webcam window, passing in the name of your new subfolder. Press the spacebar to take at least 10 pictures of your face from different angles. When you're done, **ESC** to close the window. Repeat this step to add more friends, creating a separate folder for each person.

## Step 2: Train the model

    python3 encode_faces.py

Run this command to analyze the photos and output a new file `encodings.pickle` that contains criteria for identifying these faces.

## Step 3: Test the model

    python3 facial_rec_with_voice.py

Run this command to open a new webcam window. If your face is highlighted with a yellow box alongside your name, the model has been properly trained. Hit **q** to quit the program.
