# Splunk Searches

## Hunt for hdoor.exe Execution

```spl
index=botsv3 hdoor.exe
```

---

## Process Creation Activity

```spl
index=botsv3 EventCode=1 Image="*hdoor.exe"
```

---

## Encoded PowerShell Execution

```spl
index=botsv3 powershell.exe "*enc*"
```

---

## Parent-Child Process Analysis

```spl
index=botsv3 hdoor.exe
| table _time ParentImage Image CommandLine User
```

---

## Network Activity Associated with hdoor.exe

```spl
index=botsv3 hdoor.exe
| table _time sa da dp pn ppn
```

---

## Network Discovery Activity

```spl
index=botsv3 hdoor.exe "*192.168.*"
```

---

## Timeline Reconstruction

```spl
index=botsv3 hdoor.exe
| sort _time
```
