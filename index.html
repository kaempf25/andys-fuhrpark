<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Andys Fuhrpark</title>
  <!-- React und ReactDOM -->
  <script src="https://unpkg.com/react@17/umd/react.production.min.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script>
  <!-- Tailwind CSS (optional für Styling) -->
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
  <div id="root"></div>
  <script src="app.js"></script>
</body>
</html>
import React, { useState, useEffect } from 'react';
import ReactDOM from 'react-dom';

// Fahrzeugdaten inklusive technischer Details, Bilder (Platzhalter) und Typ
const vehiclesDataInitial = [
  {
    id: 'mercedes-w113',
    name: 'Mercedes W113 230 SL (Pagode)',
    type: 'Auto',
    technical: 'Klassischer 230 SL mit originalem Motor und eleganten Linien.',
    imageUrl: 'https://via.placeholder.com/300?text=Mercedes+W113+230+SL'
  },
  {
    id: 'mercedes-r107',
    name: 'Mercedes R107 560 SL',
    type: 'Auto',
    technical: 'Leistungsstarker 560 SL, luxuriös und robust.',
    imageUrl: 'https://via.placeholder.com/300?text=Mercedes+R107+560+SL'
  },
  {
    id: 'mercedes-r129',
    name: 'Mercedes R129 500 SL',
    type: 'Auto',
    technical: 'Sportlich-eleganter 500 SL mit modernem Komfort.',
    imageUrl: 'https://via.placeholder.com/300?text=Mercedes+R129+500+SL'
  },
  {
    id: 'mercedes-w208',
    name: 'Mercedes W208 230 CLK',
    type: 'Auto',
    technical: 'Kompakter 230 CLK mit dynamischem Design.',
    imageUrl: 'https://via.placeholder.com/300?text=Mercedes+W208+230+CLK'
  },
  {
    id: 'vw-t6',
    name: 'VW Bus T6 2.0 TDI (2017)',
    type: 'Auto',
    technical: 'Robuster VW Bus mit sparsamen 2.0 TDI, ideal für Reisen.',
    imageUrl: 'https://via.placeholder.com/300?text=VW+Bus+T6+2.0+TDI'
  },
  {
    id: 'man-traktor',
    name: 'MAN Traktor 2N1',
    type: 'Landmaschine',
    technical: 'Leistungsstarker Traktor, vielseitig und robust im Landbetrieb.',
    imageUrl: 'https://via.placeholder.com/300?text=MAN+Traktor+2N1'
  },
  {
    id: 'bmw-r80',
    name: 'BMW R80 Strich 7 (1984)',
    type: 'Motorrad',
    technical: 'Klassische BMW Maschine, robust und zeitlos im Design.',
    imageUrl: 'https://via.placeholder.com/300?text=BMW+R80+Strich+7'
  },
  {
    id: 'bmw-r1200gs',
    name: 'BMW R1200GS (2014)',
    type: 'Motorrad',
    technical: 'Moderne Abenteuermaschine, zuverlässig und komfortabel.',
    imageUrl: 'https://via.placeholder.com/300?text=BMW+R1200GS'
  },
  {
    id: 'vespa-gts300',
    name: 'Vespa GTS 300',
    type: 'Roller',
    technical: 'Stilvoller Roller, ideal für die Stadt, kombiniert klassischen Charme mit moderner Technik.',
    imageUrl: 'https://via.placeholder.com/300?text=Vespa+GTS+300'
  }
];

// Standard-Wartungsaufgaben
const defaultMaintenanceTasks = [
  "Ölwechsel", "Zündkerzen prüfen", "Bremsen kontrollieren", "Reifendruck prüfen"
];

function AndysFuhrpark() {
  // Fahrzeuge laden (aus localStorage, falls schon vorhanden)
  const [vehiclesData, setVehiclesData] = useState(() => {
    const saved = localStorage.getItem('vehiclesData');
    return saved ? JSON.parse(saved) : vehiclesDataInitial;
  });
  
  // Aktives Fahrzeug, Wartungskalender-Daten (Struktur: { [vehicleId]: { [year]: { [task]: timestamp|null } } })
  const [activeVehicle, setActiveVehicle] = useState(vehiclesData[0].id);
  const [maintenanceData, setMaintenanceData] = useState(() => {
    const saved = localStorage.getItem('maintenanceData');
    return saved ? JSON.parse(saved) : {};
  });
  const [selectedYear, setSelectedYear] = useState(2025);

  // Speichere Änderungen in localStorage
  useEffect(() => {
    localStorage.setItem('maintenanceData', JSON.stringify(maintenanceData));
  }, [maintenanceData]);

  useEffect(() => {
    localStorage.setItem('vehiclesData', JSON.stringify(vehiclesData));
  }, [vehiclesData]);

  // Funktion, um den Status einer Wartungsaufgabe umzuschalten (hinzufügen/entfernen eines Datums)
  const handleTaskToggle = (vehicleId, year, task) => {
    setMaintenanceData(prev => {
      const vehicleData = prev[vehicleId] || {};
      const yearData = vehicleData[year] || {};
      const currentStatus = yearData[task];
      const newYearData = { ...yearData, [task]: currentStatus ? null : new Date().toISOString() };
      return {
        ...prev,
        [vehicleId]: {
          ...vehicleData,
          [year]: newYearData
        }
      };
    });
  };

  // Auswahl des aktiven Fahrzeugs
  const activeVehicleData = vehiclesData.find(v => v.id === activeVehicle);

  // Erstelle Array für Jahre 2025 bis 2050
  const years = [];
  for (let y = 2025; y <= 2050; y++) {
    years.push(y);
  }

  // Funktion zum Hochladen eines eigenen Bildes
  const handleImageUpload = (e) => {
    const file = e.target.files[0];
    if (file) {
      const reader = new FileReader();
      reader.onloadend = () => {
        const newImageUrl = reader.result;
        const updatedVehicles = vehiclesData.map(vehicle => {
          if (vehicle.id === activeVehicle) {
            return { ...vehicle, imageUrl: newImageUrl };
          }
          return vehicle;
        });
        setVehiclesData(updatedVehicles);
        // Ohne kompletten Reload – der State wird aktualisiert
      };
      reader.readAsDataURL(file);
    }
  };

  return (
    <div className="p-4">
      <h1 className="text-2xl font-bold mb-4">Andys Fuhrpark</h1>

      {/* Fahrzeugauswahl */}
      <div className="mb-4">
        <label className="mr-2">Fahrzeug wählen:</label>
        <select value={activeVehicle} onChange={(e) => setActiveVehicle(e.target.value)}>
          {vehiclesData.map(vehicle => (
            <option key={vehicle.id} value={vehicle.id}>{vehicle.name}</option>
          ))}
        </select>
      </div>

      {/* Fahrzeugkarte */}
      <div className="mb-4">
        <Card>
          <img src={activeVehicleData.imageUrl} alt={activeVehicleData.name} className="w-full h-auto"/>
          <CardContent>
            <h2 className="text-xl font-semibold">{activeVehicleData.name}</h2>
            <p>{activeVehicleData.technical}</p>
          </CardContent>
        </Card>
      </div>

      {/* Wartungskalender */}
      <div className="mb-4">
        <label className="mr-2">Wartungskalender Jahr:</label>
        <select value={selectedYear} onChange={(e) => setSelectedYear(parseInt(e.target.value))}>
          {years.map(year => (
            <option key={year} value={year}>{year}</option>
          ))}
        </select>
      </div>

      {/* Wartungsaufgabenliste */}
      <div>
        <h3 className="text-lg font-bold mb-2">Wartungsaufgaben für {selectedYear}</h3>
        <ul>
          {defaultMaintenanceTasks.map(task => {
            const completedDate = maintenanceData[activeVehicle] &&
              maintenanceData[activeVehicle][selectedYear] &&
              maintenanceData[activeVehicle][selectedYear][task];
            return (
              <li key={task} className="mb-2">
                <label>
                  <input
                    type="checkbox"
                    checked={!!completedDate}
                    onChange={() => handleTaskToggle(activeVehicle, selectedYear, task)}
                  />
                  <span className="ml-2">
                    {task} {completedDate && <span className="text-green-600">(Erledigt am {new Date(completedDate).toLocaleDateString()})</span>}
                  </span>
                </label>
              </li>
            );
          })}
        </ul>
      </div>

      {/* Bild-Upload */}
      <div className="mt-4">
        <h3 className="text-lg font-bold mb-2">Bild hochladen</h3>
        <input type="file" accept="image/*" onChange={handleImageUpload} />
      </div>
    </div>
  );
}

// Einfache Card-Komponente (kann bei Bedarf durch UI-Bibliotheken ersetzt werden)
function Card({ children }) {
  return <div className="border rounded shadow p-4">{children}</div>;
}

function CardContent({ children }) {
  return <div className="p-2">{children}</div>;
}

// Rendering der App
ReactDOM.render(<AndysFuhrpark />, document.getElementById('root'));
