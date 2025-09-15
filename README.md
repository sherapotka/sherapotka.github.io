import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { GraduationCap, Mail, Github, Linkedin, Award, BookOpen, Briefcase, FileText, Globe } from "lucide-react";

// ————————————————————————————————————————————————
// SHERA POTKA — Academic Homepage (single-file React)
// Design goals: minimalist, credible, recruiter-friendly, mobile-first
// Tech: TailwindCSS + shadcn/ui (available in this environment)
// Deployment: 1) Drop into a React/Vite app OR 2) Ask and I’ll provide a static HTML export
// ————————————————————————————————————————————————

const publications = [
  {
    title: "Community Structure and Coherence in Digital Humanities Works",
    venue: "IISA 2023 (14th International Conference on Information, Intelligence, Systems & Applications)",
    highlights: ["Best Paper Award", "Text-similarity networks over a decade of DH papers"],
    links: [{ label: "Venue", href: "https://doi.org/IISA2023" }],
  },
  {
    title: "Enhancing Structural Minority Visibility in Link Recommendations (MinWalk)",
    venue: "MEDES 2024 (16th International Conference on Management of Digital EcoSystems)",
    highlights: ["Best Paper Award", "Fairness + popularity-bias mitigation"],
    links: [{ label: "Venue", href: "https://medes2024.com" }],
  },
  {
    title: "Word Embedding Bias in Large Language Models",
    venue: "I-SPAN 2025 (17th International Symposium on Pervasive Systems, Algorithms, and Networks)",
    highlights: ["SC-WEAT across modern LLM embeddings"],
    links: [{ label: "Venue", href: "https://ispan2025.com" }],
  },
  {
    title: "Gender and Race Bias in Consumer Product Recommendations by Large Language Models",
    venue: "AINA 2025 (39th International Conference on Advanced Information Networking and Applications)",
    highlights: ["Bias & diversity in AI recommenders"],
    links: [{ label: "Venue", href: "#" }],
  },
  {
    title: "CluSanT: Differentially Private and Semantically Coherent Text Sanitization",
    venue: "NAACL 2025 (Americas Chapter of the ACL)",
    highlights: ["Metric Local DP", "Privacy × semantics via clustering + embeddings"],
    links: [{ label: "Conference", href: "https://2025.emnlp.org" }],
  },
];

const experience = [
  {
    role: "Instructor — Data Models & Algorithms",
    org: "University of Victoria",
    time: "Jan–Apr 2025",
    bullets: [
      "Interactive lectures with active learning",
      "Modern slides, notes, and project resources",
      "Mentored teams applying algorithms in projects",
    ],
  },
  {
    role: "Teaching Assistant — Data Mining & Web Design",
    org: "University of Victoria",
    time: "2023–2024",
    bullets: [
      "Supported cohorts up to 180 students",
      "Designed hands-on labs and grading rubrics",
      "Guided projects in ML and front‑end fundamentals",
    ],
  },
  {
    role: "Software Developer",
    org: "CCEH, University of Cologne",
    time: "Nov 2022 – Nov 2023",
    bullets: [
      "Cross‑disciplinary research software",
      "RACIR project support (higher‑ed research)",
    ],
  },
  {
    role: "Research Assistant — Digital Scholarship (ETCL)",
    org: "University of Victoria",
    time: "Oct 2022 – Mar 2023",
    bullets: [
      "WordPress visualizations & research communications",
      "Led HSS Commons project coordination",
    ],
  },
  {
    role: "Web Designer",
    org: "Junger Anleger (Cologne)",
    time: "Mar 2021 – Sep 2022",
    bullets: [
      "WordPress + Elementor sites",
      "Content & event support",
    ],
  },
];

const skills = {
  languages: ["Java", "Python", "C/C++", "Objective‑C", "C#", "SQL", "JavaScript", "HTML", "PHP"],
  tools: [".NET", "React", "Node.js", "WordPress", "Elementor Pro", "Postgres", "MySQL", "Protégé"],
};

export default function SheraAcademicSite() {
  return (
    <div className="min-h-screen bg-white text-slate-900">
      {/* Top bar */}
      <header className="sticky top-0 z-40 bg-white/80 backdrop-blur border-b">
        <div className="mx-auto max-w-6xl px-4 py-3 flex items-center justify-between">
          <a href="#home" className="font-semibold tracking-tight">Shera Potka</a>
          <nav className="hidden md:flex gap-6 text-sm">
            <a href="#research" className="hover:underline">Research</a>
            <a href="#publications" className="hover:underline">Publications</a>
            <a href="#experience" className="hover:underline">Experience</a>
            <a href="#teaching" className="hover:underline">Teaching</a>
            <a href="#contact" className="hover:underline">Contact</a>
          </nav>
          <div className="flex items-center gap-2">
            <Button asChild className="rounded-xl">
              <a href="/cv.pdf" target="_blank" rel="noreferrer">
                <FileText className="mr-2 h-4 w-4" /> CV
              </a>
            </Button>
          </div>
        </div>
      </header>

      {/* Hero */}
      <section id="home" className="relative">
        <div className="absolute inset-0 bg-gradient-to-b from-slate-50 to-white" aria-hidden />
        <div className="mx-auto max-w-6xl px-4 py-14 md:py-20 grid md:grid-cols-[1.2fr,0.8fr] gap-8 items-center">
          <div>
            <div className="inline-flex items-center gap-2 rounded-full border px-3 py-1 text-xs font-medium">
              <Award className="h-3.5 w-3.5" /> 2× Best Paper Award
            </div>
            <h1 className="mt-4 text-3xl md:text-5xl font-semibold tracking-tight">
              Fairness • Bias • Privacy in AI
            </h1>
            <p className="mt-4 text-slate-700 md:text-lg max-w-2xl">
              PhD researcher and educator focusing on data mining, algorithmic fairness, bias detection in large language models, and privacy‑preserving NLP. I build practical, ethical AI methods—and teach them to large, diverse cohorts.
            </p>
            <div className="mt-6 flex flex-wrap gap-3">
              <Button asChild variant="default" className="rounded-xl">
                <a href="#publications"><BookOpen className="mr-2 h-4 w-4"/> See publications</a>
              </Button>
              <Button asChild variant="secondary" className="rounded-xl">
                <a href="#contact"><Mail className="mr-2 h-4 w-4"/> Contact</a>
              </Button>
            </div>
            {/* Metrics */}
            <div className="mt-8 grid grid-cols-2 sm:grid-cols-4 gap-4">
              {[
                { k: "Courses supported", v: "450+" },
                { k: "Students mentored", v: "500+" },
                { k: "Best paper awards", v: "2" },
                { k: "Pubs (2023–2025)", v: "5" },
              ].map((m) => (
                <Card key={m.k} className="rounded-2xl">
                  <CardContent className="p-4">
                    <div className="text-2xl font-semibold">{m.v}</div>
                    <div className="text-xs text-slate-600">{m.k}</div>
                  </CardContent>
                </Card>
              ))}
            </div>
          </div>

          {/* Portrait & quick links */}
          <div className="flex md:justify-end">
            <div className="w-full max-w-xs mx-auto md:mx-0">
              <div className="aspect-[4/5] rounded-3xl overflow-hidden shadow-sm border bg-gradient-to-br from-slate-100 to-white flex items-center justify-center">
                <span className="text-6xl" role="img" aria-label="avatar">👩‍💻</span>
              </div>
              <div className="mt-4 grid grid-cols-3 gap-2">
                <a className="inline-flex items-center justify-center gap-2 rounded-xl border px-3 py-2 text-sm" href="mailto:spotka@uvic.ca"><Mail className="h-4 w-4"/>Email</a>
                <a className="inline-flex items-center justify-center gap-2 rounded-xl border px-3 py-2 text-sm" href="https://github.com/sherapotka" target="_blank" rel="noreferrer"><Github className="h-4 w-4"/>GitHub</a>
                <a className="inline-flex items-center justify-center gap-2 rounded-xl border px-3 py-2 text-sm" href="https://linkedin.com/in/shera-potka" target="_blank" rel="noreferrer"><Linkedin className="h-4 w-4"/>LinkedIn</a>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Research focus */}
      <section id="research" className="mx-auto max-w-6xl px-4 py-12 md:py-16">
        <div className="mb-6 flex items-center gap-2">
          <GraduationCap className="h-5 w-5" />
          <h2 className="text-xl md:text-2xl font-semibold">Research Focus</h2>
        </div>
        <div className="grid md:grid-cols-3 gap-6">
          {[
            {
              title: "Fairness in Social Recommenders",
              body: "Improving minority visibility and countering popularity bias while preserving utility.",
            },
            {
              title: "Bias in Large Language Models",
              body: "Measuring gender & race bias in embeddings and contextual models (e.g., SC‑WEAT).",
            },
            {
              title: "Privacy in NLP",
              body: "Differentially private text sanitization that maintains semantic coherence (e.g., CluSanT).",
            },
          ].map((b) => (
            <Card key={b.title} className="rounded-2xl h-full">
              <CardContent className="p-6">
                <div className="font-medium mb-1">{b.title}</div>
                <p className="text-sm text-slate-700">{b.body}</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Publications */}
      <section id="publications" className="mx-auto max-w-6xl px-4 py-12 md:py-16">
        <div className="mb-6 flex items-center gap-2">
          <BookOpen className="h-5 w-5" />
          <h2 className="text-xl md:text-2xl font-semibold">Selected Publications</h2>
        </div>
        <div className="grid gap-4">
          {publications.map((p) => (
            <Card key={p.title} className="rounded-2xl">
              <CardContent className="p-6">
                <div className="flex flex-wrap items-center justify-between gap-3">
                  <h3 className="font-medium leading-snug md:text-lg">{p.title}</h3>
                  <div className="flex gap-2">
                    {p.links?.map((l) => (
                      <a key={l.href} href={l.href} target="_blank" rel="noreferrer" className="text-sm underline inline-flex items-center gap-1"><Globe className="h-4 w-4"/>{l.label}</a>
                    ))}
                  </div>
                </div>
                <div className="mt-1 text-sm text-slate-600">{p.venue}</div>
                {p.highlights?.length ? (
                  <ul className="mt-3 flex flex-wrap gap-2 text-xs text-slate-700">
                    {p.highlights.map((h) => (
                      <li key={h} className="inline-flex items-center gap-1 rounded-full border px-2 py-1">{h}</li>
                    ))}
                  </ul>
                ) : null}
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Experience & Teaching */}
      <section id="experience" className="mx-auto max-w-6xl px-4 py-12 md:py-16">
        <div className="mb-6 flex items-center gap-2">
          <Briefcase className="h-5 w-5" />
          <h2 className="text-xl md:text-2xl font-semibold">Experience</h2>
        </div>
        <div className="grid gap-4">
          {experience.map((e) => (
            <Card key={e.role + e.time} className="rounded-2xl">
              <CardContent className="p-6">
                <div className="flex flex-wrap items-baseline justify-between gap-3">
                  <h3 className="font-medium leading-snug md:text-lg">{e.role}</h3>
                  <div className="text-sm text-slate-600">{e.time}</div>
                </div>
                <div className="text-sm text-slate-700">{e.org}</div>
                <ul className="mt-3 list-disc pl-5 text-sm text-slate-700 space-y-1">
                  {e.bullets.map((b) => (
                    <li key={b}>{b}</li>
                  ))}
                </ul>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      <section id="teaching" className="mx-auto max-w-6xl px-4 py-12 md:py-16">
        <div className="mb-6 flex items-center gap-2">
          <GraduationCap className="h-5 w-5" />
          <h2 className="text-xl md:text-2xl font-semibold">Teaching Snapshot</h2>
        </div>
        <div className="grid gap-4 md:grid-cols-3">
          <Card className="rounded-2xl"><CardContent className="p-6"><div className="text-2xl font-semibold">Instructor</div><div className="text-sm text-slate-600 mt-1">Data Models & Algorithms (UVic)</div></CardContent></Card>
          <Card className="rounded-2xl"><CardContent className="p-6"><div className="text-2xl font-semibold">TA</div><div className="text-sm text-slate-600 mt-1">Data Mining, Web Design</div></CardContent></Card>
          <Card className="rounded-2xl"><CardContent className="p-6"><div className="text-2xl font-semibold">Cohorts</div><div className="text-sm text-slate-600 mt-1">Up to 180 students</div></CardContent></Card>
        </div>
      </section>

      {/* Contact */}
      <section id="contact" className="mx-auto max-w-6xl px-4 py-12 md:py-16">
        <div className="mb-6 flex items-center gap-2">
          <Mail className="h-5 w-5" />
          <h2 className="text-xl md:text-2xl font-semibold">Get in touch</h2>
        </div>
        <Card className="rounded-2xl">
          <CardContent className="p-6 md:p-8 flex flex-col md:flex-row md:items-center md:justify-between gap-6">
            <div>
              <div className="text-lg font-medium">spotka@uvic.ca</div>
              <div className="text-sm text-slate-600">Victoria, BC · Open to collaborations, teaching, and research partnerships</div>
            </div>
            <div className="flex gap-3">
              <Button asChild className="rounded-xl"><a href="mailto:spotka@uvic.ca"><Mail className="mr-2 h-4 w-4"/>Email</a></Button>
              <Button asChild variant="secondary" className="rounded-xl"><a href="https://linkedin.com/in/shera-potka" target="_blank" rel="noreferrer"><Linkedin className="mr-2 h-4 w-4"/>LinkedIn</a></Button>
              <Button asChild variant="secondary" className="rounded-xl"><a href="https://github.com/sherapotka" target="_blank" rel="noreferrer"><Github className="mr-2 h-4 w-4"/>GitHub</a></Button>
            </div>
          </CardContent>
        </Card>
      </section>

      {/* Footer */}
      <footer className="border-t">
        <div className="mx-auto max-w-6xl px-4 py-8 text-xs text-slate-500 flex flex-wrap items-center gap-3 justify-between">
          <div>© {new Date().getFullYear()} Shera Potka</div>
          <div className="flex gap-4">
            <a className="underline" href="/cv.pdf">CV</a>
            <a className="underline" href="#publications">Publications</a>
            <a className="underline" href="#research">Research</a>
          </div>
        </div>
      </footer>
    </div>
  );
}
