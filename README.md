#include <iostream>

class PlatePledge {
private:
    int totalPlates;
    int pledgedPlates;

public:
    PlatePledge() : totalPlates(0), pledgedPlates(0) {}

    void pledgePlate() {
        totalPlates++;
        pledgedPlates++;
    }

    float getProgress() {
        return (float(pledgedPlates) / float(totalPlates)) * 100;
    }
};

int main() {
    PlatePledge platePledge;
    platePledge.pledgePlate();
    std::cout << "Progress: " << platePledge.getProgress() << "%" << std::endl;
    return 0;
}
