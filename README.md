# Summit Platform

A free, open-source virtual summit platform with speaker directory, event management, registrations, and giveaways. A complete alternative to EventRaptor, built with Next.js and Supabase.

## Features

### For Event Hosts
- **Event Management** - Create and manage summits, workshops, webinars, and meetings
- - **Speaker Directory** - Browse and invite speakers from a searchable directory
  - - **Registration System** - Automated registration with customizable forms
    - - **Attendee Analytics** - Track registrations, attendance, and engagement
      - - **Affiliate Tracking** - Built-in affiliate system for promotional partners
       
        - ### For Speakers
        - - **Speaker Profiles** - Create professional profiles with bio, credentials, and presentations
          - - **Speaking Opportunities** - Discover and apply to events seeking speakers
            - - **Presentation Showcase** - Display your talks with descriptions and booking links
              - - **Event History** - Show your speaking experience and past events
               
                - ### For Attendees
                - - **Event Discovery** - Browse upcoming summits and events
                  - - **Easy Registration** - One-click registration with saved profiles
                    - - **Giveaway Participation** - Enter giveaways associated with events
                     
                      - ## Tech Stack
                     
                      - - **Framework**: Next.js 14 (App Router)
                        - - **Database**: PostgreSQL via Prisma ORM
                          - - **Authentication**: NextAuth.js v5
                            - - **Styling**: Tailwind CSS + shadcn/ui
                              - - **Deployment**: Vercel / Railway / Any Node.js host
                               
                                - ## Quick Start
                               
                                - ### Prerequisites
                                - - Node.js 18+
                                  - - PostgreSQL database (or use Supabase free tier)
                                   
                                    - ### Installation
                                   
                                    - 1. **Clone the repository**
                                      2.    ```bash
                                               git clone https://github.com/alexhitt/summit-platform.git
                                               cd summit-platform
                                               ```

                                            2. **Install dependencies**
                                            3.    ```bash
                                                     npm install
                                                     ```

                                                  3. **Set up environment variables**
                                                  4.    ```bash
                                                           cp .env.example .env.local
                                                           ```

                                                              Fill in your database URL and auth credentials:
                                                       ```
                                                 DATABASE_URL="postgresql://..."
                                           NEXTAUTH_SECRET="your-secret-key"
                                         NEXTAUTH_URL="http://localhost:3000"
                                         ```

                                         4. **Set up the database**
                                            ```bash
                                            npx prisma generate
                                            npx prisma db push
                                            ```

                                         5. **Run the development server**
                                            ```bash
                                            npm run dev
                                            ```

                                         Visit `http://localhost:3000` to see your summit platform!

                                         ## Project Structure

                                         ```
                                         summit-platform/
                                      ├── app/                    # Next.js App Router pages
                                      │   ├── (auth)/            # Authentication pages
                                      │   ├── (dashboard)/       # Dashboard pages
                                      │   ├── events/            # Event directory & pages
                                      │   ├── speakers/          # Speaker directory & profiles
                                      │   ├── giveaways/         # Giveaway directory
                                      │   └── api/               # API routes
                                      ├── components/            # React components
                                      │   ├── ui/               # shadcn/ui components
                                      │   ├── events/           # Event-related components
                                      │   ├── speakers/         # Speaker-related components
                                      │   └── forms/            # Form components
                                      ├── lib/                   # Utility functions
                                      │   ├── db.ts             # Prisma client
                                      │   ├── auth.ts           # NextAuth configuration
                                      │   └── utils.ts          # Helper functions
                                      ├── prisma/               # Database schema
                                      │   └── schema.prisma     # Prisma schema file
                                      └── public/               # Static assets
                                      ```

                                      ## Database Schema

                                      The platform includes models for:
                                      - **Users** - Authentication and user management
                                      - **Speaker Profiles** - Professional speaker information
                                      - **Presentations** - Speaker talks and topics
                                      - **Events** - Summits, workshops, webinars
                                      - **Registrations** - Event registrations
                                      - **Giveaways** - Promotional giveaways
                                      - **Affiliates** - Tracking referrals
                                      - **Business Areas & Topics** - Categorization system

                                      ## Free Hosting Options

                                      ### Database (Free Tier)
                                      - [Supabase](https://supabase.com) - 500MB free
                                      - [Neon](https://neon.tech) - 512MB free
                                      - [Railway](https://railway.app) - $5 credit

                                      ### Application Hosting (Free Tier)
                                      - [Vercel](https://vercel.com) - Best for Next.js
                                      - [Railway](https://railway.app) - Full-stack hosting
                                      - [Render](https://render.com) - Web services

                                      ## Contributing

                                      Contributions are welcome! Please read our contributing guidelines before submitting PRs.

                                      ## License

                                      MIT License - feel free to use this for your own summit platform!

                                      ## Roadmap

                                      - [ ] Email automation (registration confirmations, reminders)
                                      - [ ] Video hosting integration
                                      - [ ] Ticket sales / paid registrations
                                      - [ ] Calendar integrations
                                      - [ ] Mobile app
                                      - [ ] Embeddable widgets for external sites

                                      ---

                                      Built with ❤️ as a free alternative to paid summit platforms.
