import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import {
  PhoneCall,
  MessageCircle,
  MapPin
} from "lucide-react";

export default function KSMRServices() {
  const handleSubmit = (e: React.FormEvent<HTMLFormElement>) => {
    e.preventDefault();
    // Handle form submission logic here (e.g., API call, validation, toast)
    alert("Message submitted! We’ll get back to you soon.");
  };

  return (
    <main className="font-sans p-6 space-y-10">
      <header className="text-center space-y-2">
        <h1 className="text-4xl font-bold text-blue-700">KSMR Services</h1>
        <p className="text-lg text-gray-600">
          Your one-stop solution for Broking Services, Online Store & More
        </p>
      </header>

      <nav
        aria-label="Main Navigation"
        className="flex justify-center gap-6 text-blue-600 font-semibold"
      >
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#gallery">Gallery</a>
        <a href="#testimonials">Testimonials</a>
        <a href="#blog">Blog</a>
        <a href="#contact">Contact</a>
      </nav>

      <section id="home" className="text-center space-y-4">
        <h2 className="text-3xl font-bold">Welcome to KSMR Services</h2>
        <p>
          We offer broking solutions including real estate, medical support,
          online store products, and more across India.
        </p>
      </section>

      <section id="about" className="space-y-3">
        <h2 className="text-2xl font-bold">About Us</h2>
        <p>
          KSMR Services connects customers with trusted service providers across
          categories -- real estate, medical, vehicles, gold, furniture, and
          more. We work PAN India with a focus on quality and convenience.
        </p>
      </section>

      <section id="services" className="space-y-5">
        <h2 className="text-2xl font-bold">Our Services</h2>
        <ul className="list-disc list-inside space-y-1">
          <li>Farmhouse broking</li>
          <li>Medical hospital tie-ups</li>
          <li>Car detailing</li>
          <li>Real estate (Land, Flat, Plot)</li>
          <li>Online store (Gold, Furniture, Electronics)</li>
          <li>Girls hostel references</li>
          <li>Dog sellers</li>
        </ul>
      </section>

      <section id="gallery" className="space-y-4">
        <h2 className="text-2xl font-bold">Gallery</h2>
        <div className="grid grid-cols-2 md:grid-cols-3 gap-4">
          {[1, 2, 3].map((item) => (
            <img
              key={item}
              src={`https://via.placeholder.com/200?text=Gallery+${item}`}
              alt={`Gallery image ${item}`}
              className="rounded-xl"
              loading="lazy"
            />
          ))}
        </div>
      </section>

      <section id="testimonials" className="space-y-3">
        <h2 className="text-2xl font-bold">Client Reviews</h2>
        <Card>
          <CardContent className="p-4">
            Great service! Helped me with a hospital reference within minutes. —{" "}
            <strong>Rahul M.</strong>
          </CardContent>
        </Card>
        <Card>
          <CardContent className="p-4">
            Got my dream plot through KSMR broking. Very responsive team. —{" "}
            <strong>Priya S.</strong>
          </CardContent>
        </Card>
      </section>

      <section id="blog" className="space-y-3">
        <h2 className="text-2xl font-bold">Latest Blog</h2>
        <Card>
          <CardContent className="p-4 space-y-2">
            <h3 className="text-xl font-semibold">
              Tips for Buying Your First Plot
            </h3>
            <p>
              Location, budget, and paperwork — here's what you must check
              before investing in real estate...
            </p>
            <Button variant="link">Read More</Button>
          </CardContent>
        </Card>
      </section>

      <section id="contact" className="space-y-3">
        <h2 className="text-2xl font-bold">Contact Us</h2>
        <form onSubmit={handleSubmit} className="space-y-3">
          <Input placeholder="Your Name" name="name" required aria-label="Name" />
          <Input
            placeholder="Email Address"
            name="email"
            type="email"
            required
            aria-label="Email Address"
          />
          <Textarea
            placeholder="Your Message"
            name="message"
            rows={4}
            required
            aria-label="Message"
          />
          <Button type="submit">Submit</Button>
        </form>
        <div className="flex items-center gap-2 pt-4">
          <PhoneCall className="text-green-500" />{" "}
          <a href="tel:+919000000000">+91 90000 00000</a>
        </div>
        <div className="flex items-center gap-2">
          <MessageCircle className="text-green-500" />{" "}
          <a href="https://wa.me/919000000000">Chat on WhatsApp</a>
        </div>
        <div className="flex items-center gap-2">
          <MapPin className="text-red-500" /> <span>Hyderabad, India</span>
        </div>
      </section>
    </main>
  );
}
