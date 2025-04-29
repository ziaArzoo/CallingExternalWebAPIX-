# Weather API Integration in Dynamics 365 F&O

This project contains a sample X++ class that demonstrates how to call the **Open-Meteo** weather API using `System.Net.HttpWebRequest` in **Microsoft Dynamics 365 Finance & Operations** (D365 F&O). It fetches current weather data based on latitude and longitude.

## 📄 Class: `WebServSysopService`

### 🔧 Functionality

- Makes a **GET request** to the [Open-Meteo API](https://open-meteo.com/) for current weather data.
- Uses `System.Net.HttpWebRequest`, `System.Net.WebHeaderCollection`, and `.NET stream readers`.
- Includes support for **Authorization headers** (Bearer Token).
- Parses the response using `FormJsonSerializer`.

---

### 🔍 Method Details

#### `getLink(real _long = 28.61, real _lat = 77.23)`

Generates the full API URL using given coordinates (defaults to Delhi, India).

#### `startoperation(WebServSysopContract _contract)`

1. Builds the HTTP request with headers.
2. Sends the request and reads the JSON response.
3. Deserializes the response into a custom class `WeatherJsonDeserializerHeader`.
4. Extracts and displays the latitude from the response.

---

### ✅ Sample Output

