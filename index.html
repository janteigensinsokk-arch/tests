import { useState, useEffect } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import ReactMarkdown from "react-markdown";

// Example JSON file structure (docs.json)
// [
//   { "id": "intro", "title": "Introduction", "file": "intro.md" },
//   { "id": "setup", "title": "Setup", "file": "setup.md" },
//   { "id": "usage", "title": "Usage", "file": "usage.md" }
// ]

export default function Documentation() {
  const [tabs, setTabs] = useState([]);
  const [activeTab, setActiveTab] = useState(null);
  const [content, setContent] = useState("");

  useEffect(() => {
    // Load tabs from JSON
    fetch("/docs.json")
      .then((res) => res.json())
      .then((data) => {
        setTabs(data);
        if (data.length > 0) {
          setActiveTab(data[0]);
        }
      });
  }, []);

  useEffect(() => {
    if (activeTab) {
      fetch(`/${activeTab.file}`)
        .then((res) => res.text())
        .then((md) => setContent(md));
    }
  }, [activeTab]);

  return (
    <div className="grid grid-cols-4 min-h-screen">
      {/* Sidebar */}
      <aside className="col-span-1 bg-gray-100 p-4 border-r">
        <h2 className="text-xl font-bold mb-4">Docs</h2>
        <div className="flex flex-col space-y-2">
          {tabs.map((tab) => (
            <Button
              key={tab.id}
              variant={activeTab?.id === tab.id ? "default" : "outline"}
              onClick={() => setActiveTab(tab)}
            >
              {tab.title}
            </Button>
          ))}
        </div>
      </aside>

      {/* Content */}
      <main className="col-span-3 p-6">
        <Card className="shadow-md">
          <CardContent>
            <article className="prose max-w-none">
              <ReactMarkdown>{content}</ReactMarkdown>
            </article>
          </CardContent>
        </Card>
      </main>
    </div>
  );
}
