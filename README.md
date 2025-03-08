# LA-GUAJIRA-COLOMBIA
PROCESOS DE LEY
import React, { useState } from 'react';

export default function LaGuajiraApp() {
  const [showRestitutionAreas, setShowRestitutionAreas] = useState(false);

  const toggleRestitutionAreas = () => {
    setShowRestitutionAreas(!showRestitutionAreas);
  };

  return (
    <div className="bg-gray-100 min-h-screen p-8">
      <header className="mb-8">
        <h1 className="text-3xl font-semibold text-gray-800">La Guajira, Colombia</h1>
        <p className="text-gray-600">A glimpse into its land, people, and challenges.</p>
      </header>

      <section className="bg-white rounded-lg shadow-md p-6 mb-8">
        <h2 className="text-xl font-medium text-gray-700 mb-4">Overview</h2>
        <p className="text-gray-800 leading-relaxed">
          The department of La Guajira encompasses approximately 2,084,800 hectares, featuring a diverse geography that includes desert areas, mountain ranges, valleys, and Caribbean coasts. It is the ancestral home of the Wayuu indigenous people and holds potential in sectors such as mining, tourism, and agriculture.
        </p>
      </section>

      <section className="bg-white rounded-lg shadow-md p-6 mb-8">
        <h2 className="text-xl font-medium text-gray-700 mb-4">Conflict and Restitution</h2>
        <p className="text-gray-800 leading-relaxed mb-4">
          However, armed conflict and land dispossession have affected several populations, creating the need for land restitution processes.
        </p>

        <button
          className="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"
          onClick={toggleRestitutionAreas}
        >
          {showRestitutionAreas ? 'Hide Restitution Areas' : 'Show Restitution Areas'}
        </button>

        {showRestitutionAreas && (
          <div className="mt-4">
            <h3 className="text-lg font-semibold text-gray-700 mb-2">Key Restitution Areas:</h3>
            <ul className="list-disc list-inside text-gray-800">
              <li>Fonseca</li>
              <li>San Juan del Cesar</li>
              <li>Dibulla</li>
              <li>Wayuu Indigenous Reserves</li>
              <li>Maicao</li>
              <li>Uribia</li>
            </ul>
            <p className="text-gray-600 mt-2">
              These areas face disputes over land related to mining and territorial control. The restitution process seeks to guarantee the return of communities to their lands, recognize indigenous territorial rights, and recover ecosystems affected by conflict and land misuse.
            </p>
          </div>
        )}
      </section>

      <footer className="text-center text-gray-500 mt-8">
        <p>&copy; 2024 La Guajira App</p>
      </footer>
    </div>
  );
}
