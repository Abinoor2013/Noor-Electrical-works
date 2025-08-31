noor_electrical_site/
  index.html
  images/
    logo.png
    team.jpgimport React from "react";

// Noor Electrical Bathinda - Single-file React component
// TailwindCSS utility classes used (no import needed in this preview)
// Replace PAYMENT_HANDLER with real payment integration (Razorpay/Stripe) when deploying

export default function NoorElectricalWebsite() {
  const services = [
    { id: 1, name: "Fan Installation", price: "â‚¹250", desc: "Ceiling & Wall fan installation with wiring check." },
    { id: 2, name: "Light / Tube Fitting", price: "â‚¹150", desc: "Tube light / Bulb installation + LED fitting." },
    { id: 3, name: "Wiring / Rewiring", price: "â‚¹1,500", desc: "2BHK basic rewiring (material extra)." },
    { id: 4, name: "AC Installation", price: "â‚¹800", desc: "Split AC installation + mounting & gas check." },
    { id: 5, name: "PIR Sensor Lamp", price: "â‚¹500", desc: "Motion sensor lamp installation & setup." },
    { id: 6, name: "Repair & Troubleshoot", price: "Call for Quote", desc: "Earthing, short-circuit, switchboard repair." }
  ];

  function handleBook(service) {
    // Placeholder payment / booking flow
    // In production connect to Razorpay/Stripe or your backend
    alert(`Booking requested:\nService: ${service.name} \nPrice: ${service.price} \nContact: 9781364000`);
  }

  return (
    <div className="min-h-screen bg-gray-50 text-gray-900 font-sans">
      <header className="bg-gradient-to-r from-yellow-400 to-orange-500 shadow-md">
        <div className="max-w-5xl mx-auto px-4 py-6 flex items-center justify-between">
          <div className="flex items-center gap-4">
            <div className="w-12 h-12 rounded-full bg-white flex items-center justify-center font-bold text-orange-500">N</div>
            <div>
              <h1 className="text-white text-xl font-bold">Noor Electrical Bathinda</h1>
              <p className="text-yellow-100 text-sm">Fan / Light / Wiring / AC â€” 24x7 Service</p>
            </div>
          </div>

          <div className="hidden md:flex items-center gap-4">
            <a href="tel:9781364000" className="bg-white text-orange-600 px-4 py-2 rounded shadow">Call: 9781364000</a>
            <a href="mailto:lakhvinder.hunjra@gmail.com" className="text-white underline">lakhvinder.hunjra@gmail.com</a>
          </div>
        </div>
      </header>

      <main className="max-w-5xl mx-auto px-4 py-8">
        {/* Hero */}
        <section className="grid md:grid-cols-2 gap-6 items-center mb-8">
          <div>
            <h2 className="text-3xl font-extrabold">Punjabi vich service â€” bharosemand, sasti te tez</h2>
            <p className="mt-4 text-gray-700">Noor Electrical Bathinda vich assi fan installation, tube-fitting, wiring, AC installation, repair te commercial electrical solutions provide karde haan. 24x7 emergency support te guarantee.</p>

            <div className="mt-6 flex gap-3">
              <a href="#services" className="bg-orange-500 text-white px-4 py-2 rounded shadow">Services vekho</a>
              <a href="https://wa.me/919781364000" className="bg-green-500 text-white px-4 py-2 rounded shadow">WhatsApp te book karo</a>
            </div>
          </div>

          <div className="bg-white rounded shadow p-4">
            <h3 className="font-semibold">Quick Contact</h3>
            <p className="text-sm text-gray-600">Call / WhatsApp for fastest response</p>
            <div className="mt-3">
              <a href="tel:9781364000" className="block bg-gray-100 px-3 py-2 rounded mb-2">ðŸ“ž 9781364000</a>
              <a href="mailto:lakhvinder.hunjra@gmail.com" className="block bg-gray-100 px-3 py-2 rounded">âœ‰ï¸ lakhvinder.hunjra@gmail.com</a>
            </div>
          </div>
        </section>

        {/* Services */}
        <section id="services" className="mb-10">
          <h3 className="text-2xl font-bold mb-4">Saadi Services</h3>
          <div className="grid md:grid-cols-3 gap-4">
            {services.map(s => (
              <div key={s.id} className="bg-white p-4 rounded shadow">
                <h4 className="font-semibold">{s.name}</h4>
                <p className="text-sm text-gray-600 mt-1">{s.desc}</p>
                <div className="mt-3 flex items-center justify-between">
                  <div className="text-lg font-bold">{s.price}</div>
                  <div className="flex gap-2">
                    <button onClick={() => handleBook(s)} className="bg-orange-500 text-white px-3 py-1 rounded">Book</button>
                    <a href={`https://wa.me/919781364000?text=Hello%20Noor%20Electrical,%20I%20want%20to%20book%20${encodeURIComponent(s.name)}`} className="bg-green-500 text-white px-3 py-1 rounded">WhatsApp</a>
                  </div>
                </div>
              </div>
            ))}
          </div>
        </section>

        {/* About */}
        <section className="mb-10 bg-white p-6 rounded shadow">
          <h3 className="text-2xl font-bold mb-2">About Noor Electrical</h3>
          <p className="text-gray-700">Main Lakhvinder Singh, Noor Electrical Services â€” Bathinda. Assi 10+ saal da tajurba rakhde haan. Har kam nu guarantee mil di hai. Contact: 9781364000.</p>
        </section>

        {/* Testimonials */}
        <section className="mb-10">
          <h3 className="text-2xl font-bold mb-4">Reviews</h3>
          <div className="grid md:grid-cols-2 gap-4">
            <div className="bg-white p-4 rounded shadow">
              <p className="text-gray-700">"Fast service te fair price â€” fan installation bahut vadia hoya."</p>
              <p className="mt-2 text-sm font-semibold">â€” S. Kaur, Bathinda</p>
            </div>
            <div className="bg-white p-4 rounded shadow">
              <p className="text-gray-700">"AC mount karan da kam professional te safe si."</p>
              <p className="mt-2 text-sm font-semibold">â€” R. Singh, Bathinda</p>
            </div>
          </div>
        </section>

        {/* Contact Form */}
        <section className="mb-16 bg-white p-6 rounded shadow">
          <h3 className="text-2xl font-bold mb-4">Contact Form</h3>
          <form onSubmit={(e) => { e.preventDefault(); alert('Form submit: We will call you soon (placeholder).'); }}>
            <div className="grid md:grid-cols-2 gap-3">
              <input required placeholder="Tuhada Naam" className="p-2 border rounded" />
              <input required placeholder="Phone (9781364000)" className="p-2 border rounded" />
              <input placeholder="Email (optional)" className="p-2 border rounded" />
              <input placeholder="Shehar" className="p-2 border rounded" />
            </div>
            <textarea placeholder="Message / Service details" className="mt-3 p-2 border rounded w-full" rows={4}></textarea>
            <div className="mt-3 flex gap-3">
              <button type="submit" className="bg-orange-500 text-white px-4 py-2 rounded">Send</button>
              <a href="https://wa.me/919781364000" className="bg-green-500 text-white px-4 py-2 rounded">WhatsApp te book karo</a>
            </div>
          </form>
        </section>

      </main>

      <footer className="bg-gray-900 text-white py-6">
        <div className="max-w-5xl mx-auto px-4 flex flex-col md:flex-row justify-between items-center">
          <div>
            <div className="font-bold">Noor Electrical Services</div>
            <div className="text-sm">Baba Deep Singh Nagar, Gali No. 2/1, near FCI Godown, Bathinda</div>
            <div className="text-sm">Phone: 9781364000 | Email: lakhvinder.hunjra@gmail.com</div>
          </div>
          <div className="mt-4 md:mt-0 text-sm">Â© {new Date().getFullYear()} Noor Electrical Bathinda</div>
        </div>
      </footer>
    </div>
  );
}


