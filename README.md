# Chroma-PV-Simulator-Automation
Controlling Chroma PV simulator with MATLAB
Include the ChromaController.m class in your current working directory and create chroma object
like this 
% Create an instance of EquipmentController
chroma = ChromaController('USB0::0x0A69::0x084B::S01000065535::0::INSTR');

Establish the connection  with the following command

% Connect to the instrument
chroma = chroma.connect();

after the connection is established, use the following methods to perform the operations
chroma.turnOn();
chroma.turnOff();
chroma.setPower(1500);

finally, use the command below to disconnect
% Disconnect from the instrument
chroma.disconnect();


Note:
in order for the above code to work, you IVI drivers for chroma must be installed.
