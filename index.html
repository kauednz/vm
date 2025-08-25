import React, { useState, useEffect } from 'react';
import { Calendar, DollarSign, Users, FileText, Plus, Trash2, Edit, Save, X, Download, Globe } from 'lucide-react';

const VentureMCloudPlatform = () => {
  const [language, setLanguage] = useState('pt');
  const [houses, setHouses] = useState([]);
  const [dailyServices, setDailyServices] = useState([]);
  const [activeTab, setActiveTab] = useState('houses');
  const [selectedDate, setSelectedDate] = useState(new Date().toISOString().split('T')[0]);
  const [editingHouse, setEditingHouse] = useState(null);
  const [newHouse, setNewHouse] = useState({ name: '', address: '', value: '', clientName: '', phone: '', notes: '' });

  // Translations
  const translations = {
    pt: {
      title: "Venture MCloud - Gestão de Limpeza",
      subtitle: "Controle de serviços e pagamentos",
      housesTab: "Casas Cadastradas",
      dailyTab: "Serviços Diários",
      reportsTab: "Relatórios",
      manageHouses: "Gerenciar Casas",
      addNewHouse: "Adicionar Nova Casa",
      houseName: "Nome da casa",
      address: "Endereço",
      value: "Valor ($)",
      clientName: "Nome do cliente",
      phone: "Telefone",
      notes: "Observações",
      add: "Adicionar",
      dailyServices: "Serviços Diários",
      selectHouse: "Selecionar casa...",
      dayTotal: "Total do Dia:",
      teamReports: "Relatórios por Equipe",
      last7Days: "Últimos 7 dias:",
      weekTotal: "Total 7 dias:",
      noServices: "Nenhum serviço",
      exportPdf: "Exportar PDF",
      santos: "Santos",
      regiane: "Regiane"
    },
    en: {
      title: "Venture MCloud - Cleaning Management",
      subtitle: "Service and payment control",
      housesTab: "Registered Houses",
      dailyTab: "Daily Services",
      reportsTab: "Reports",
      manageHouses: "Manage Houses",
      addNewHouse: "Add New House",
      houseName: "House name",
      address: "Address",
      value: "Value ($)",
      clientName: "Client name",
      phone: "Phone",
      notes: "Notes",
      add: "Add",
      dailyServices: "Daily Services",
      selectHouse: "Select house...",
      dayTotal: "Day Total:",
      teamReports: "Team Reports",
      last7Days: "Last 7 days:",
      weekTotal: "7-day Total:",
      noServices: "No services",
      exportPdf: "Export PDF",
      santos: "Santos",
      regiane: "Regiane"
    }
  };

  const t = translations[language];

  // Initialize with sample data
  useEffect(() => {
    if (houses.length === 0) {
      setHouses([
        { 
          id: 1, 
          name: 'Silva Residence', 
          address: '123 Oak Street, Downtown', 
          value: 150,
          clientName: 'Maria Silva',
          phone: '+1 (555) 123-4567',
          notes: 'Pet-friendly house, 2 cats'
        },
        { 
          id: 2, 
          name: 'Johnson Apartment', 
          address: '456 Central Ave, Apt 5B', 
          value: 120,
          clientName: 'John Johnson',
          phone: '+1 (555) 234-5678',
          notes: 'High-rise apartment, elevator access'
        },
        { 
          id: 3, 
          name: 'Santos Family Home', 
          address: '789 Green Lane', 
          value: 200,
          clientName: 'Carlos Santos',
          phone: '+1 (555) 345-6789',
          notes: 'Large house, pool area included'
        },
        { 
          id: 4, 
          name: 'Corporate Office Lima', 
          address: '321 Business Center', 
          value: 180,
          clientName: 'Lima Corp',
          phone: '+1 (555) 456-7890',
          notes: 'Office building, after hours cleaning'
        },
        { 
          id: 5, 
          name: 'Brown Townhouse', 
          address: '654 Maple Street', 
          value: 135,
          clientName: 'Jennifer Brown',
          phone: '+1 (555) 567-8901',
          notes: '3-story townhouse'
        }
      ]);
    }
  }, [houses.length]);

  const addHouse = () => {
    if (newHouse.name && newHouse.address && newHouse.value) {
      const house = {
        id: Date.now(),
        name: newHouse.name,
        address: newHouse.address,
        value: parseFloat(newHouse.value),
        clientName: newHouse.clientName,
        phone: newHouse.phone,
        notes: newHouse.notes
      };
      setHouses([...houses, house]);
      setNewHouse({ name: '', address: '', value: '', clientName: '', phone: '', notes: '' });
    }
  };

  const deleteHouse = (id) => {
    setHouses(houses.filter(h => h.id !== id));
  };

  const updateHouse = (id, updatedHouse) => {
    setHouses(houses.map(h => h.id === id ? { ...h, ...updatedHouse } : h));
    setEditingHouse(null);
  };

  const addDailyService = (houseId, team) => {
    const service = {
      id: Date.now(),
      houseId,
      team,
      date: selectedDate,
      house: houses.find(h => h.id === houseId)
    };
    setDailyServices([...dailyServices, service]);
  };

  const removeDailyService = (serviceId) => {
    setDailyServices(dailyServices.filter(s => s.id !== serviceId));
  };

  const getTeamServices = (team, date) => {
    return dailyServices.filter(s => s.team === team && s.date === date);
  };

  const calculateTeamTotal = (team, date) => {
    return getTeamServices(team, date).reduce((total, service) => {
      return total + (service.house?.value || 0);
    }, 0);
  };

  const generatePDFReport = (team) => {
    const last7Days = Array.from({length: 7}, (_, i) => {
      const date = new Date();
      date.setDate(date.getDate() - i);
      const dateStr = date.toISOString().split('T')[0];
      const services = getTeamServices(team, dateStr);
      const total = calculateTeamTotal(team, dateStr);
      
      return {
        date: new Date(dateStr).toLocaleDateString(language === 'pt' ? 'pt-BR' : 'en-US', { 
          weekday: 'long', 
          year: 'numeric',
          month: 'long', 
          day: 'numeric' 
        }),
        services: services.map(s => ({
          house: s.house?.name,
          client: s.house?.clientName,
          value: s.house?.value
        })),
        total
      };
    });

    const weekTotal = last7Days.reduce((sum, day) => sum + day.total, 0);

    // Create PDF content
    const pdfContent = `
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Venture MCloud - ${team} Report</title>
    <style>
        body { 
            font-family: Arial, sans-serif; 
            margin: 20px;
            color: #333;
        }
        .header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #2563eb;
        }
        .company-name {
            color: #2563eb;
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 5px;
        }
        .report-title {
            font-size: 18px;
            color: #666;
        }
        .team-name {
            font-size: 20px;
            color: #2563eb;
            margin: 20px 0 15px 0;
            font-weight: bold;
        }
        .day-section {
            margin-bottom: 20px;
            padding: 15px;
            border: 1px solid #e5e7eb;
            border-radius: 8px;
        }
        .day-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
            font-weight: bold;
        }
        .day-date {
            color: #374151;
        }
        .day-total {
            color: #059669;
            font-size: 16px;
        }
        .services-list {
            margin-left: 20px;
        }
        .service-item {
            display: flex;
            justify-content: space-between;
            margin: 5px 0;
            padding: 5px 0;
        }
        .service-details {
            color: #6b7280;
        }
        .service-value {
            color: #059669;
            font-weight: bold;
        }
        .week-total {
            margin-top: 30px;
            padding: 20px;
            background-color: #f3f4f6;
            border-radius: 8px;
            text-align: center;
            font-size: 18px;
            font-weight: bold;
            color: #2563eb;
        }
        .no-services {
            color: #9ca3af;
            font-style: italic;
        }
        .footer {
            margin-top: 40px;
            text-align: center;
            color: #9ca3af;
            font-size: 12px;
        }
    </style>
</head>
<body>
    <div class="header">
        <div class="company-name">VENTURE MCLOUD</div>
        <div class="report-title">${t.teamReports}</div>
        <div class="team-name">${language === 'pt' ? 'Equipe' : 'Team'} ${team}</div>
        <div style="color: #6b7280; font-size: 14px;">
            ${new Date().toLocaleDateString(language === 'pt' ? 'pt-BR' : 'en-US', {
              year: 'numeric',
              month: 'long',
              day: 'numeric'
            })}
        </div>
    </div>

    ${last7Days.map(day => `
        <div class="day-section">
            <div class="day-header">
                <span class="day-date">${day.date}</span>
                <span class="day-total">$${day.total.toFixed(2)}</span>
            </div>
            ${day.services.length > 0 ? `
                <div class="services-list">
                    ${day.services.map(service => `
                        <div class="service-item">
                            <div>
                                <strong>${service.house}</strong>
                                <div class="service-details">${service.client}</div>
                            </div>
                            <span class="service-value">$${service.value.toFixed(2)}</span>
                        </div>
                    `).join('')}
                </div>
            ` : `
                <div class="no-services">${t.noServices}</div>
            `}
        </div>
    `).join('')}

    <div class="week-total">
        ${t.weekTotal} $${weekTotal.toFixed(2)}
    </div>

    <div class="footer">
        Generated by Venture MCloud Platform - ${new Date().toLocaleString(language === 'pt' ? 'pt-BR' : 'en-US')}
    </div>
</body>
</html>`;

    // Create and download PDF
    const blob = new Blob([pdfContent], { type: 'text/html' });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = `VentureMCloud_${team}_Report_${new Date().toISOString().split('T')[0]}.html`;
    document.body.appendChild(a);
    a.click();
    document.body.removeChild(a);
    URL.revokeObjectURL(url);
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-100">
      <div className="container mx-auto p-6">
        <div className="bg-white rounded-lg shadow-lg overflow-hidden">
          {/* Header */}
          <div className="bg-gradient-to-r from-blue-600 to-indigo-600 text-white p-6">
            <div className="flex justify-between items-center">
              <div>
                <h1 className="text-2xl font-bold flex items-center gap-2">
                  <Users className="w-6 h-6" />
                  {t.title}
                </h1>
                <p className="text-blue-100 mt-1">{t.subtitle}</p>
              </div>
              <div className="flex items-center gap-4">
                <button
                  onClick={() => setLanguage(language === 'pt' ? 'en' : 'pt')}
                  className="flex items-center gap-2 bg-blue-500 hover:bg-blue-400 px-3 py-2 rounded-lg transition-colors"
                >
                  <Globe className="w-4 h-4" />
                  {language === 'pt' ? 'English' : 'Português'}
                </button>
              </div>
            </div>
          </div>

          {/* Navigation */}
          <div className="border-b border-gray-200">
            <nav className="flex">
              {[
                { id: 'houses', label: t.housesTab, icon: DollarSign },
                { id: 'daily', label: t.dailyTab, icon: Calendar },
                { id: 'reports', label: t.reportsTab, icon: FileText }
              ].map(({ id, label, icon: Icon }) => (
                <button
                  key={id}
                  onClick={() => setActiveTab(id)}
                  className={`flex items-center gap-2 px-6 py-4 font-medium transition-colors ${
                    activeTab === id
                      ? 'border-b-2 border-blue-500 text-blue-600 bg-blue-50'
                      : 'text-gray-600 hover:text-blue-600 hover:bg-gray-50'
                  }`}
                >
                  <Icon className="w-4 h-4" />
                  {label}
                </button>
              ))}
            </nav>
          </div>

          <div className="p-6">
            {/* Houses Database */}
            {activeTab === 'houses' && (
              <div>
                <div className="mb-6">
                  <h2 className="text-xl font-semibold mb-4">{t.manageHouses}</h2>
                  
                  {/* Add new house */}
                  <div className="bg-gray-50 p-4 rounded-lg mb-4">
                    <h3 className="font-medium mb-3">{t.addNewHouse}</h3>
                    <div className="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-6 gap-3">
                      <input
                        type="text"
                        placeholder={t.houseName}
                        value={newHouse.name}
                        onChange={(e) => setNewHouse({...newHouse, name: e.target.value})}
                        className="border border-gray-300 rounded-lg px-3 py-2"
                      />
                      <input
                        type="text"
                        placeholder={t.address}
                        value={newHouse.address}
                        onChange={(e) => setNewHouse({...newHouse, address: e.target.value})}
                        className="border border-gray-300 rounded-lg px-3 py-2"
                      />
                      <input
                        type="number"
                        placeholder={t.value}
                        value={newHouse.value}
                        onChange={(e) => setNewHouse({...newHouse, value: e.target.value})}
                        className="border border-gray-300 rounded-lg px-3 py-2"
                      />
                      <input
                        type="text"
                        placeholder={t.clientName}
                        value={newHouse.clientName}
                        onChange={(e) => setNewHouse({...newHouse, clientName: e.target.value})}
                        className="border border-gray-300 rounded-lg px-3 py-2"
                      />
                      <input
                        type="text"
                        placeholder={t.phone}
                        value={newHouse.phone}
                        onChange={(e) => setNewHouse({...newHouse, phone: e.target.value})}
                        className="border border-gray-300 rounded-lg px-3 py-2"
                      />
                      <input
                        type="text"
                        placeholder={t.notes}
                        value={newHouse.notes}
                        onChange={(e) => setNewHouse({...newHouse, notes: e.target.value})}
                        className="border border-gray-300 rounded-lg px-3 py-2"
                      />
                    </div>
                    <button
                      onClick={addHouse}
                      className="mt-3 bg-blue-600 text-white rounded-lg px-4 py-2 hover:bg-blue-700 flex items-center gap-2"
                    >
                      <Plus className="w-4 h-4" />
                      {t.add}
                    </button>
                  </div>

                  {/* Houses list */}
                  <div className="grid gap-3">
                    {houses.map(house => (
                      <div key={house.id} className="border border-gray-200 rounded-lg p-4">
                        {editingHouse === house.id ? (
                          <div className="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-6 gap-3">
                            <input
                              type="text"
                              defaultValue={house.name}
                              onChange={(e) => setEditingHouse({...house, name: e.target.value})}
                              className="border border-gray-300 rounded-lg px-3 py-2"
                            />
                            <input
                              type="text"
                              defaultValue={house.address}
                              onChange={(e) => setEditingHouse({...house, address: e.target.value})}
                              className="border border-gray-300 rounded-lg px-3 py-2"
                            />
                            <input
                              type="number"
                              defaultValue={house.value}
                              onChange={(e) => setEditingHouse({...house, value: parseFloat(e.target.value)})}
                              className="border border-gray-300 rounded-lg px-3 py-2"
                            />
                            <input
                              type="text"
                              defaultValue={house.clientName}
                              onChange={(e) => setEditingHouse({...house, clientName: e.target.value})}
                              className="border border-gray-300 rounded-lg px-3 py-2"
                            />
                            <input
                              type="text"
                              defaultValue={house.phone}
                              onChange={(e) => setEditingHouse({...house, phone: e.target.value})}
                              className="border border-gray-300 rounded-lg px-3 py-2"
                            />
                            <input
                              type="text"
                              defaultValue={house.notes}
                              onChange={(e) => setEditingHouse({...house, notes: e.target.value})}
                              className="border border-gray-300 rounded-lg px-3 py-2"
                            />
                            <div className="flex gap-2 col-span-full">
                              <button
                                onClick={() => updateHouse(house.id, editingHouse)}
                                className="bg-green-600 text-white rounded-lg px-3 py-2 hover:bg-green-700"
                              >
                                <Save className="w-4 h-4" />
                              </button>
                              <button
                                onClick={() => setEditingHouse(null)}
                                className="bg-gray-600 text-white rounded-lg px-3 py-2 hover:bg-gray-700"
                              >
                                <X className="w-4 h-4" />
                              </button>
                            </div>
                          </div>
                        ) : (
                          <div className="flex justify-between items-start">
                            <div className="grid md:grid-cols-3 gap-4 flex-1">
                              <div>
                                <h3 className="font-medium text-blue-600">{house.name}</h3>
                                <p className="text-gray-600 text-sm">{house.address}</p>
                              </div>
                              <div>
                                <p className="font-medium">{house.clientName}</p>
                                <p className="text-gray-600 text-sm">{house.phone}</p>
                              </div>
                              <div>
                                <p className="text-gray-600 text-sm">{house.notes}</p>
                              </div>
                            </div>
                            <div className="flex items-center gap-3 ml-4">
                              <span className="text-lg font-semibold text-green-600">
                                ${house.value.toFixed(2)}
                              </span>
                              <button
                                onClick={() => setEditingHouse(house.id)}
                                className="text-blue-600 hover:bg-blue-50 p-1 rounded"
                              >
                                <Edit className="w-4 h-4" />
                              </button>
                              <button
                                onClick={() => deleteHouse(house.id)}
                                className="text-red-600 hover:bg-red-50 p-1 rounded"
                              >
                                <Trash2 className="w-4 h-4" />
                              </button>
                            </div>
                          </div>
                        )}
                      </div>
                    ))}
                  </div>
                </div>
              </div>
            )}

            {/* Daily Services */}
            {activeTab === 'daily' && (
              <div>
                <div className="mb-6">
                  <div className="flex justify-between items-center mb-4">
                    <h2 className="text-xl font-semibold">{t.dailyServices}</h2>
                    <input
                      type="date"
                      value={selectedDate}
                      onChange={(e) => setSelectedDate(e.target.value)}
                      className="border border-gray-300 rounded-lg px-3 py-2"
                    />
                  </div>

                  {/* Teams */}
                  <div className="grid md:grid-cols-2 gap-6">
                    {['Santos', 'Regiane'].map(team => (
                      <div key={team} className="border border-gray-200 rounded-lg p-4">
                        <h3 className="font-semibold mb-4 text-blue-600">
                          {language === 'pt' ? 'Equipe' : 'Team'} {team}
                        </h3>
                        
                        {/* Add service */}
                        <div className="mb-4">
                          <select
                            onChange={(e) => {
                              if (e.target.value) {
                                addDailyService(parseInt(e.target.value), team);
                                e.target.value = '';
                              }
                            }}
                            className="w-full border border-gray-300 rounded-lg px-3 py-2"
                          >
                            <option value="">{t.selectHouse}</option>
                            {houses.map(house => (
                              <option key={house.id} value={house.id}>
                                {house.name} - {house.clientName} - ${house.value.toFixed(2)}
                              </option>
                            ))}
                          </select>
                        </div>

                        {/* Day services */}
                        <div className="space-y-2">
                          {getTeamServices(team, selectedDate).map(service => (
                            <div key={service.id} className="flex justify-between items-center bg-gray-50 p-3 rounded">
                              <div>
                                <span className="font-medium">{service.house?.name}</span>
                                <p className="text-sm text-gray-600">{service.house?.clientName}</p>
                                <p className="text-xs text-gray-500">{service.house?.address}</p>
                              </div>
                              <div className="flex items-center gap-2">
                                <span className="text-green-600 font-medium">
                                  ${service.house?.value.toFixed(2)}
                                </span>
                                <button
                                  onClick={() => removeDailyService(service.id)}
                                  className="text-red-600 hover:bg-red-50 p-1 rounded"
                                >
                                  <Trash2 className="w-4 h-4" />
                                </button>
                              </div>
                            </div>
                          ))}
                        </div>

                        {/* Team total */}
                        <div className="mt-4 pt-4 border-t border-gray-200">
                          <div className="flex justify-between items-center">
                            <span className="font-semibold">{t.dayTotal}</span>
                            <span className="text-xl font-bold text-green-600">
                              ${calculateTeamTotal(team, selectedDate).toFixed(2)}
                            </span>
                          </div>
                        </div>
                      </div>
                    ))}
                  </div>
                </div>
              </div>
            )}

            {/* Reports */}
            {activeTab === 'reports' && (
              <div>
                <h2 className="text-xl font-semibold mb-6">{t.teamReports}</h2>
                
                <div className="grid md:grid-cols-2 gap-6">
                  {['Santos', 'Regiane'].map(team => (
                    <div key={team} className="border border-gray-200 rounded-lg p-4">
                      <div className="flex justify-between items-center mb-4">
                        <h3 className="font-semibold text-blue-600">
                          {language === 'pt' ? 'Equipe' : 'Team'} {team}
                        </h3>
                        <button
                          onClick={() => generatePDFReport(team)}
                          className="flex items-center gap-2 bg-green-600 text-white px-3 py-2 rounded-lg hover:bg-green-700 text-sm"
                        >
                          <Download className="w-4 h-4" />
                          {t.exportPdf}
                        </button>
                      </div>
                      
                      <p className="text-sm text-gray-600 mb-3">{t.last7Days}</p>
                      
                      {/* Last 7 days */}
                      <div className="space-y-3">
                        {Array.from({length: 7}, (_, i) => {
                          const date = new Date();
                          date.setDate(date.getDate() - i);
                          const dateStr = date.toISOString().split('T')[0];
                          const services = getTeamServices(team, dateStr);
                          const total = calculateTeamTotal(team, dateStr);
                          
                          return (
                            <div key={dateStr} className="bg-gray-50 p-3 rounded">
                              <div className="flex justify-between items-center mb-2">
                                <span className="font-medium">
                                  {new Date(dateStr).toLocaleDateString(language === 'pt' ? 'pt-BR' : 'en-US', { 
                                    weekday: 'short', 
                                    day: '2-digit', 
                                    month: '2-digit' 
                                  })}
                                </span>
                                <span className="text-green-600 font-semibold">
                                  ${total.toFixed(2)}
                                </span>
                              </div>
                              {services.length > 0 && (
                                <div className="text-sm text-gray-600">
                                  {services.map(s => `${s.house?.name} (${s.house?.clientName})`).join(', ')}
                                </div>
                              )}
                              {services.length === 0 && (
                                <div className="text-sm text-gray-400">{t.noServices}</div>
                              )}
                            </div>
                          );
                        })}
                      </div>

                      {/* Week total */}
                      <div className="mt-4 pt-4 border-t border-gray-200">
                        <div className="flex justify-between items-center">
                          <span className="font-semibold">{t.weekTotal}</span>
                          <span className="text-xl font-bold text-blue-600">
                            ${Array.from({length: 7}, (_, i) => {
                              const date = new Date();
                              date.setDate(date.getDate() - i);
                              return calculateTeamTotal(team, date.toISOString().split('T')[0]);
                            }).reduce((a, b) => a + b, 0).toFixed(2)}
                          </span>
                        </div>
                      </div>
                    </div>
                  ))}
                </div>
              </div>
            )}
          </div>
        </div>
      </div>
    </div>
  );
};

export default VentureMCloudPlatform;