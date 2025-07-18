# idempotency-python-module
This repository is a idempotency module for python idempotent function

# How to use
to make a function idempotent, just implement the ***@idempotency*** decorator (name of the idempotency module).
### Example code
```py
from idenpotenceFuncionUtils import idempotency

@idempotency
async def startAudioMeeting(**kwargs):
    recordingMeeting = recordMicrophoneAudio()

    if recordingMeeting is None:
        raise HTTPException(status_code=404, detail="Audio file is null or not found.")

    return recordingMeeting
```
