import React, { useMemo, useState } from 'react';

export default function BirthdayWebsite() {
  const [isOpen, setIsOpen] = useState(false);

  const hearts = useMemo(
    () => Array.from({ length: 40 }, (_, i) => ({
      id: i,
      left: `${Math.random() * 100}%`,
      delay: `${Math.random() * 5}s`,
      size: `${16 + Math.random() * 20}px`,
    })),
    []
  );

  const memories = [
    'The Day You Made Me Smile 😊',
    'Our Cute Conversations 💬',
    'Every Moment With You ❤️',
    'Forever My Favourite Person ✨',
  ];

  return (
    <main className="relative min-h-screen overflow-hidden bg-black text-white">
      <div className="absolute inset-0 bg-[radial-gradient(circle_at_top,rgba(255,0,102,0.18),transparent_40%)]" />
      <div className="absolute inset-0 bg-[radial-gradient(circle_at_bottom,rgba(168,85,247,0.15),transparent_40%)]" />

      <div className="pointer-events-none absolute inset-0 overflow-hidden">
        {hearts.map((heart) => (
          <span
            key={heart.id}
            className="absolute animate-pulse opacity-70"
            style={{
              left: heart.left,
              top: `${Math.random() * 100}%`,
              animationDelay: heart.delay,
              fontSize: heart.size,
            }}
          >
            ✨
          </span>
        ))}
      </div>

      <section className="relative flex min-h-screen items-center justify-center px-6 text-center">
        <div className="relative z-10 max-w-5xl">
          <div className="mb-6 inline-flex rounded-full border border-pink-400/20 bg-pink-500/10 px-6 py-2 backdrop-blur-md">
            <span className="text-sm tracking-[0.2em] text-pink-300 uppercase">
              A Magical Birthday Surprise For My Love 💖
            </span>
          </div>

          <h1 className="text-6xl font-black leading-[1.1] tracking-tight md:text-8xl">
            <span className="block text-white drop-shadow-[0_0_30px_rgba(255,255,255,0.15)]">
              Happy Birthday
            </span>
            <span className="bg-gradient-to-r from-pink-300 via-rose-400 to-fuchsia-500 bg-clip-text text-transparent drop-shadow-[0_0_50px_rgba(255,0,128,0.35)]">
              Bachha ❤️, My Love
            </span>
          </h1>

          <p className="mx-auto mt-8 max-w-3xl text-xl leading-9 text-gray-300 md:text-2xl">
            Today is not just your birthday. It’s the day the most beautiful soul
            came into my world and made everything feel softer, warmer and happier ❤️
          </p>

          <button
            onClick={() => setIsOpen(!isOpen)}
            className="mt-10 rounded-full bg-gradient-to-r from-pink-500 to-rose-500 px-10 py-5 text-lg font-bold shadow-[0_0_40px_rgba(255,0,100,0.4)] transition duration-300 hover:scale-110"
          >
            🎁 Open Birthday Surprise
          </button>

          {isOpen && (
            <div className="mt-10 rounded-[2.5rem] border border-pink-400/20 bg-white/10 p-10 backdrop-blur-xl shadow-[0_0_70px_rgba(255,0,128,0.15)]">
              <div className="text-7xl animate-bounce">🎁</div>

              <h2 className="mt-5 text-4xl font-black bg-gradient-to-r from-pink-300 to-rose-500 bg-clip-text text-transparent">
                A Little Surprise For My Love ❤️
              </h2>

              <p className="mt-5 text-lg leading-9 text-gray-200">
                Happy Birthday Bachha ❤️
                <br /><br />
                Tum meri life ki sabse beautiful blessing ho.
                Tumhare bina sab kuch adhoora sa lagta hai.
                Main bas ye chahta hoon ki tum hamesha smile karo,
                khush raho aur meri life mein hamesha aise hi raho 💖
              </p>
            </div>
          )}
        </div>
      </section>

      <section className="px-6 py-20 text-center">
        <h2 className="mb-8 text-5xl font-black tracking-tight text-pink-400">
          💌 Secret Birthday Letter
        </h2>

        <div className="relative mx-auto max-w-5xl overflow-hidden rounded-[2.5rem] border border-white/10 bg-white/5 p-12 backdrop-blur-xl shadow-[0_0_80px_rgba(255,0,120,0.1)]">
          <div className="absolute -top-16 -right-16 h-48 w-48 rounded-full bg-pink-500/10 blur-3xl" />
          <div className="absolute -bottom-20 -left-16 h-48 w-48 rounded-full bg-purple-500/10 blur-3xl" />

          <p className="relative z-10 text-xl leading-[2.2] text-gray-200 md:text-2xl">
            Happy Birthday Bachha ❤️
            <br /><br />
            My Love, aaj ka din mere liye bhi utna hi special hai jitna tumhare liye,
            kyunki aaj ke din meri duniya ka sabse beautiful person is world mein aaya tha ✨
            <br /><br />
            Main bas itna kehna chahta hoon ki tum meri life ki sabse beautiful blessing ho.
            Tumhare saath har moment magical lagta hai, aur tumhari smile meri favourite cheez hai 💖
            <br /><br />
            On your special day, meri dua hai ki tumhari life mein kabhi sadness naa aaye,
            tum hamesha smile karo, healthy raho, successful bano aur duniya ki saari happiness tumhe mile 🌸
            <br /><br />
            I wish ki tumhare saare dreams complete ho,
            har naye din tumhare liye happiness aur positivity laaye ✨
            <br /><br />
            Thank you for coming into my life and making everything feel more beautiful,
            softer and full of love ❤️
            <br /><br />
            No matter what happens,
            I will always pray for your happiness because seeing you smile is my favourite feeling 💕
            <br /><br />
            Happy Birthday once again Bachha ❤️
            You deserve all the love, happiness, peace and success in this world 🌍✨
            <br /><br />
            Forever Yours,
            <br />
            My Heart ❤️
          </p>
        </div>
      </section>
    <section className="px-6 py-20 text-center">
        <h2 className="mb-10 text-5xl font-black text-pink-400">
          💖 Reasons Why I Love You
        </h2>

        <div className="mx-auto grid max-w-5xl gap-6 md:grid-cols-3">
          {[
            'Your Smile 😊',
            'Your Cute Talks 💬',
            'How You Make Me Happy ❤️',
            'Your Caring Nature 🌸',
            'Every Moment With You ✨',
            'Because You Are You 💖',
          ].map((item) => (
            <div
              key={item}
              className="rounded-[2rem] border border-pink-400/10 bg-white/5 p-8 backdrop-blur-xl transition hover:scale-105"
            >
              <p className="text-2xl font-semibold">{item}</p>
            </div>
          ))}
        </div>
      </section>

      <section className="px-6 py-20 text-center">
        <h2 className="mb-8 text-5xl font-black text-pink-400">
          📸 Our Beautiful Memories
        </h2>

        <div className="mx-auto grid max-w-5xl gap-6 md:grid-cols-3">
          {[1, 2, 3].map((photo) => (
            <div
              key={photo}
              className="rounded-[2rem] border border-white/10 bg-white/5 p-4 shadow-2xl backdrop-blur-xl"
            >
              <div className="flex h-64 items-center justify-center rounded-[1.5rem] bg-pink-500/10 text-5xl">
                ❤️
              </div>
              <p className="mt-4 text-gray-300">Beautiful Memory {photo}</p>
            </div>
          ))}
        </div>
      </section>

      <section className="px-6 py-20 text-center">
        <h2 className="mb-8 text-5xl font-black text-pink-400">
          🎁 Special Birthday Wishes
        </h2>

        <div className="mx-auto flex max-w-5xl flex-wrap justify-center gap-4">
          {[
            {
              title: '💖 Love Wish',
              message: 'Happy Birthday My Love ❤️ Tumhari life hamesha happiness aur love se bhari rahe ✨',
            },
            {
              title: '🌸 Cute Wish',
              message: 'Tumhari smile hamesha aise hi cute aur beautiful rahe 😊💖',
            },
            {
              title: '✨ Dream Wish',
              message: 'Tumhare saare dreams complete ho aur tum life mein bahut successful bano 🌍',
            },
            {
              title: '🌙 Forever Wish',
              message: 'Main bas ye wish karta hoon ki hum hamesha saath rahein ❤️',
            },
            { title: '🎂 Birthday Wish', message: 'Aaj ka din tumhare liye duniya ki saari happiness lekar aaye 🎉' },
            { title: '🌹 Romantic Wish', message: 'Har janam mein main tumhe hi choose karun ❤️ Tum meri favourite person ho.' },
            { title: '🫶 Care Wish', message: 'Tum hamesha healthy, happy aur tension-free raho 💖' },
            { title: '⭐ Success Wish', message: 'Tum life mein bahut successful bano aur tumhari har wish puri ho ✨' },
            { title: '💫 Forever Together', message: 'Main wish karta hoon humari bonding hamesha itni hi beautiful rahe ❤️' },
          ].map((wish) => (
            <details
              key={wish.title}
              className="w-full max-w-sm rounded-[2rem] border border-pink-400/20 bg-white/5 p-5 backdrop-blur-xl transition hover:scale-105"
            >
              <summary className="cursor-pointer list-none text-xl font-semibold text-pink-300">
                {wish.title}
              </summary>

              <p className="mt-4 text-lg leading-8 text-gray-300">
                {wish.message}
              </p>
            </details>
          ))}
        </div>
      </section>

      <section className="px-6 py-20 text-center">
        <div className="mx-auto max-w-4xl rounded-[3rem] border border-pink-400/20 bg-white/5 p-12 backdrop-blur-xl shadow-[0_0_100px_rgba(255,0,120,0.12)]">
          <div className="text-7xl">🎂</div>
          <h2 className="mt-4 text-5xl font-black bg-gradient-to-r from-pink-300 via-rose-400 to-fuchsia-500 bg-clip-text text-transparent">
            Birthday Blessings For My Love ✨
          </h2>

          <p className="mt-6 text-xl leading-10 text-gray-200">
            I pray that your life is filled with endless happiness,
            beautiful moments, peace, success and lots of love ❤️
            <br /><br />
            You deserve the whole world, all the smiles,
            and every beautiful thing this life can offer 🌸
          </p>
        </div>
      </section>

      <section className="px-6 py-24 text-center">
        <div className="mx-auto max-w-4xl rounded-[3rem] border border-pink-400/20 bg-gradient-to-b from-pink-500/10 to-white/5 p-12 backdrop-blur-xl shadow-[0_0_80px_rgba(255,0,120,0.1)]">
          <h2 className="text-5xl font-black text-pink-400">
            💍 Final Surprise
          </h2>

          <p className="mt-6 text-2xl leading-10 text-gray-200">
            No matter what happens in life,
            I just want you to know that
            you will always be my favourite person,
            my comfort place,
            and the most beautiful part of my life ❤️
            <br /><br />
            Happy Birthday Once Again Bachha ✨
          </p>
        </div>
      </section>
    </main>
  );
}
