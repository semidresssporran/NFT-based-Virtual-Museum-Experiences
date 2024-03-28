# NFT-based-Virtual-Museum-Experiences
Create immersive, NFT-based virtual museum experiences that allow users to explore and interact with digital art and artifacts.
class NFT:
    def __init__(self, title, artist, year, description):
        self.title = title
        self.artist = artist
        self.year = year
        self.description = description

    def display_info(self):
        print(f"Title: {self.title}")
        print(f"Artist: {self.artist}")
        print(f"Year: {self.year}")
        print(f"Description: {self.description}\n")

class VirtualMuseum:
    def __init__(self):
        self.collection = []

    def add_nft(self, nft):
        self.collection.append(nft)

    def explore_museum(self):
        print("Welcome to the Virtual Museum of NFT Art and Artifacts")
        print("Explore our collection:\n")
        for index, nft in enumerate(self.collection, start=1):
            print(f"{index}. {nft.title} by {nft.artist} ({nft.year})")

        choice = int(input("\nEnter the number of the NFT you want to learn more about: ")) - 1
        if 0 <= choice < len(self.collection):
            self.collection[choice].display_info()
        else:
            print("Invalid choice. Please try again.")

# Sample NFTs
nft1 = NFT("Mona Lisa Tokenized", "Leonardo da Vinci", 1517, "A digital representation of the iconic Mona Lisa.")
nft2 = NFT("The Starry Night Digital", "Vincent van Gogh", 1889, "A tokenized version of Van Gogh's masterpiece.")
nft3 = NFT("The Scream in Blockchain", "Edvard Munch", 1893, "A digital artifact of Munch's famous painting.")

# Setting up the museum
virtual_museum = VirtualMuseum()
virtual_museum.add_nft(nft1)
virtual_museum.add_nft(nft2)
virtual_museum.add_nft(nft3)

# Let's explore the museum
if __name__ == "__main__":
    virtual_museum.explore_museum()
