# Searches Performed

## Search 1 - SHA256 IOC Search

### Search Value

```text id="8mfqjo"
99925199059EE049F7AEDA8904C2F5BDFBA86671FD7A5989BD60B72F26EF737C
```

### Purpose

Determine whether the SHA256 hash extracted during Investigation 03 was present within MISP threat intelligence sources.

### Result

No matching events or attributes were identified.

### Assessment

The hash was not present within the synchronized threat intelligence feeds available during the investigation.

---

## Search 2 - Filename Search

### Search Value

```text id="e9j8eh"
hdoor.exe
```

### Purpose

Determine whether the executable filename was associated with known malware, campaigns, or threat actor activity.

### Result

No matching events or attributes were identified.

### Assessment

No threat intelligence references were identified for the filename.

---

## Search 3 - Alternate Filename Search

### Search Value

```text id="zaz4oa"
hdoor
```

### Purpose

Identify any broader references that may not include the full filename.

### Result

No matching events or attributes were identified.

### Assessment

No threat intelligence references were identified.

---

## Threat Intelligence Sources

The following MISP feeds were enabled and synchronized during the investigation:

* CIRCL OSINT Feed
* Botvrij.eu OSINT Feed

---

## Investigation Summary

```text id="l7gyk9"
Investigation 03
        ↓
SHA256 Extraction
        ↓
MISP Enrichment
        ↓
Hash Search
        ↓
Filename Search
        ↓
Threat Intelligence Assessment
```

### Final Result

No threat intelligence matches were identified for the investigated hash or filename.

Behavioral evidence collected during Investigation 03 remained the primary basis for assessing the activity as suspicious.


```
```
