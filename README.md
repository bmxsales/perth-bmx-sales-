import React from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";

const bikes = [
  {
    id: 1,
    name: "Pro BMX 2000",
    price: "$399",
    image: "https://via.placeholder.com/300x200?text=Pro+BMX+2000"
  },
  {
    id: 2,
    name: "Street Blazer",
    price: "$459",
    image: "https://via.placeholder.com/300x200?text=Street+Blazer"
  },
  {
    id: 3,
    name: "Dirt King",
    price: "$499",
    image: "https://via.placeholder.com/300x200?text=Dirt+King"
  }
];

export default function BMXStore() {
  return (
    <div className="p-8 space-y-8">
      <h1 className="text-4xl font-bold text-center">BMX Bike Store</h1>
      <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
        {bikes.map((bike) => (
          <Card key={bike.id} className="rounded-2xl shadow-md">
            <CardContent className="p-4 space-y-4">
              <img
                src={bike.image}
                alt={bike.name}
                className="w-full h-48 object-cover rounded-xl"
              />
              <h2 className="text-xl font-semibold">{bike.name}</h2>
              <p className="text-lg text-green-600">{bike.price}</p>
              <Button className="w-full">Buy Now</Button>
            </CardContent>
          </Card>
        ))}
      </div>
    </div>
  );
}
